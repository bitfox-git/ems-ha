## Developing the extension

1.  setup a rathole server somewhere
2.  run the devcontainer with vscode
3.  press enter on the completed console that should have opened
4.  open a new shell and insert supervisor_run
5.  wait a couple of minutes
6.  visit localhost:7123
7.  create a admin user called akadmin
8.  go to the addon store & install the ems addon and vscode addon, enable vscode ingress in panel etc
    - make sure to configure the ems addon with the right rathole config
9.  go to the visit the vscode ui
10. edit `configuration.yaml` to add to the end

        ```
        http: !include ems.yaml
        auth_header:
            username_header: X-Forwarded-Preferred-Username
        ```

11. restart home assistant
12. mission complete!
