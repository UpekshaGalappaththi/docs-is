# Register a standard-based application

To integrate an application with {{product_name}}, you need to register it through the {{product_name}} Console. Registering a standard-based application lets you configure protocol settings (OIDC, SAML{% if product=="is"%} , WS-Fed{% endif%}) from scratch.

## Register an application

To register an application:

1. On the {{ product_name }} Console, go to **Applications**.
2. Click **New Application** and select **Standard-Based Application**.

    ![Register a standard-based application]({{base_path}}/assets/img/guides/applications/register-an-sba.png){: width="600" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

3. Provide an application name and select the other options based on your requirements.

    !!! note
        - You can choose OIDC or SAML as the standard protocol for your application. See the complete list of [OIDC]({{base_path}}/references/app-settings/oidc-settings-for-app/) and [SAML]({{base_path}}/references/app-settings/saml-settings-for-app/)  configurations.
        - If you use OIDC, you can configure a management app, which can access the management APIs in {{ product_name }}. Learn about [invoking management APIs]({{base_path}}/apis/{{ api_authentication_path }}/).

4. Click **Register** to complete the registration.

    !!! note
        If you have enabled **Allow sharing with organizations** while registering the application, you will see a popup window with the following options.

        ![Share the application with organizations]({{base_path}}/assets/img/guides/applications/share-application.png){: width="500" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

        <table>
            <tr>
                <th>Option</th>
                <th>Description</th>
            </tr>
            <tr>
                <td>Share with all organizations</td>
                <td>If selected, the application will be shared with all existing organizations and any new organizations you may create in the future.</td>
            </tr>
            <tr>
                <td>Share with only selected organizations</td>
                <td>If selected, you can select the organizations you wish to share the application with.</td>
            </tr>
        </table>

    !!! note
        If you are planning to enable the Authorization Code grant type for standard-based applications, please note the following when adding the authorized redirect URL. The authorized redirect URL should be defined based on the type of application you are using:
        
        - Web-based applications: Use exact URLs or implement logic to dynamically register specific redirect URIs as needed.
        
        - Mobile apps with deep links: Wildcard support may be acceptable, but it must be implemented securely and restricted to well-defined patterns to limit its scope.

## What's Next?

- [Configuring an OIDC application]({{base_path}}/references/app-settings/oidc-settings-for-app/)
- [Configuring a SAML application]({{base_path}}/references/app-settings/saml-settings-for-app/)