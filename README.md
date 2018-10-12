# Use docker with X display

## gui-app_root:

	- as root
	- using network_mode: host (not safe)
 
Reference: https://medium.com/@SaravSun/running-gui-applications-inside-docker-containers-83d65c0db110

## gui-app_user:

	- as host user, provided a uid (UID is shell var not a env var)


## Usage:

    dc -f docker-compose_v2.yml up -d
    docker exec -ti gui-app_root_1 bash
    # xeyes
    docker exec -ti gui-app_user_1 bash
    # xeyes
