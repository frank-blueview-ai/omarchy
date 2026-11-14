# Remmina and WayVNC connection setup

For a new Omarchy client connecting to an authenticated WayVNC server, install Remmina with its GTK-VNC (GVNC) plugin. In Remmina, create or edit the connection and select **GVNC** as the protocol, rather than **VNC**. Enter the server's resolvable hostname and the VNC username. The VNC password is configured on the server and may differ from the account's login password.

The server must present a certificate valid for the hostname used by the client. Obtain its public certificate through an authenticated, trusted channel such as SSH, verify it belongs to the intended server, and select it as the CA certificate if the client requests one. Do not copy the server's private key to the client. Keep passwords, private keys, personal profiles, private addresses, and machine-specific certificates out of this repository. Follow the local security policy for credential storage.

On 2026-11-14, a Remmina **GVNC** connection to a WayVNC server using VeNCrypt X509Plain succeeded after the regular Remmina **VNC** connection failed during authentication. The user confirmed the connection worked. The exact cause of the regular VNC plugin failure was not established; a server certificate hostname mismatch was also corrected before the successful GVNC test.

If authentication fails, confirm that the server is reachable and running, the certificate matches the hostname and is trusted, and the VNC username and password are correct. Check the server's WayVNC service logs for handshake errors. Do not disable authentication or certificate verification to work around a failure.

This note documents manual setup; it does not install packages, create a connection profile, provision certificates, or enable a remote desktop server automatically.
