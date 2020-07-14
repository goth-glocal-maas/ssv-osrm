# OSRM for Thailand

This is the stats for using the whole Thailand pdf file.

    NAME                MEM USAGE / LIMIT
    osrm_osrm_walk_1    1.101GiB / 3.846GiB
    osrm_osrm_car_1     1.036GiB / 3.846GiB
    osrm_caddy_1        3.797MiB / 3.846GiB

For the service area (around Sukhumvit area only), they are down to very minimum.

    NAME                MEM USAGE / LIMIT
    osrm_osrm_car_1     2.84MiB / 3.846GiB
    osrm_osrm_walk_1    2.914MiB / 3.846GiB
    osrm_caddy_1        3.465MiB / 3.846GiB

## Start

    docker-compose up

## Usage

All requests will be forwarded to `osrm_car` container with the exception of `/route/v1/walk/` which will be handled by `osrm_walk` container

    curl -XGET http://localhost:1180/route/v1/walk/100.5685933,13.7319484;100.5695537,13.7430816

    curl -XGET http://localhost:1180/route/v1/car/100.5685933,13.7319484;100.5695537,13.7430816
