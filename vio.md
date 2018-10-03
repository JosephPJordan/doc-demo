# Creating a Modular BIG-IP instance in VIO


## General prerequisites

Obtain a VIO account; you cannot login without first requesting an account. To request a VIO account, open a ticket at [go/pdlab](http://go/pdlab).

### Task


1. Open the VIO Seattle login page at https://vio-sea.pdsea.f5net.com/auth/login/.

   **Note**: This task is currently only available for users in Seattle.

2. For the **Domain**, retain the default (**Default**).

3. Type your Olympus credentials for **User Name** and **Password**, and then click **Connect**.

   The Overview page opens.

4. In the left pane, click **Instances**.

   The Instances page opens.

5. Click **Launch Instance**.

6. In the Launch Instance window, type an **Instance Name**, and then click **Next**.

7. From the Select Boot Source list, select **Instance Snapshot**.

8. In the Name column, click the **+ (plus sign)**  box for **mbip-openstack-1.0.5**, and then click **Next**.

9. For Flavor, click the **+ (plus sign)** box for **m1.medium**, and then click **Next**.

10. For Networks, click the **+ (plus sign)** box for **AdminNetwork2**, and then click **Next**.

11. **Optional**: Click the **Configuration** tab to include custom configuration parameters.

12. Before entering custom configuration parameters, locate the [most recent number](https://gitlab.f5net.com/mbip/mbip-bom/tags) of the `mbip-installer` to enter for `<version number>`.

    In the **Customization Script** box, copy/paste the following code, and then click **Next**.

    ```
    #cloud-config
      f5:
        mbip:
          installer:
              host: artifactory.f5net.com
              repo: f5-mbip-docker/mbip-installer
              version: <version number>
    ```

11. Click **Launch Instance**.

    The Instance page opens.

    After spawning, the Instance you created is at the top of the list.




