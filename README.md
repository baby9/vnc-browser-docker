# Alpine docker container image with VNC environments

Installed with the following components:

* Desktop environment [**Fluxbox**](http://fluxbox.org)
* vnc server (default VNC port `5901`)
* [**noVNC**](https://github.com/novnc/noVNC) - HTML5 VNC client (default http port `6901`)
* Browsers:
  * Firefox

## Usage

- Run command with mapping to local port `5901` (vnc protocol) and `6901` (vnc web access):

      docker run -d -p 5901:5901 -p 6901:6901 zenexas/vnc-browser

- Run command with mapping to local port `5901` (vnc protocol) and `6901` (vnc web access) with access password:

      docker run -d -p 5901:5901 -p 6901:6901 -e VNC_PASSWORD="vncpassword" zenexas/vnc-browser

- Run command with mapping to local port `5901` (vnc protocol) and `6901` (vnc web access) with specific resolution:

      docker run -d -p 5901:5901 -p 6901:6901 -e RESOLUTION=1600x1200 zenexas/vnc-browser

## Reference
- [tiny-remote-desktop](https://github.com/soffchen/tiny-remote-desktop)
