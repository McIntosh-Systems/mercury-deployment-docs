# Optional integrations

Administrators choose which integrations are available and which users can
connect them. Users can grant specific integration tools to individual Bots
within their access profile. Users cannot add their own MCP servers from the
Mercury client.

## Microsoft 365

Mercury sign-in grants no access to Microsoft 365 data. Connectors use a
separate Entra app. For each enabled connection, the user signs in with their
Microsoft account and completes Microsoft's consent flow for the requested
delegated permissions.

| Integration | What people and Bots can do |
| --- | --- |
| Outlook mail | Find and read messages, prepare replies, and review drafts before sending. |
| Microsoft 365 Calendar | Look up events, check availability, and create or update meetings. |
| OneDrive | Find files and read supported text files from the connected drive. |

[Preparing a meeting follow-up](using-mercury.md#preparing-a-meeting-follow-up) shows how all three can support one task.

## Specialized plugins and Spaces

DataFlow builds dashboards from supported connected data sources.

Mercury supports specialized plugins. A read-only SQL plugin for ERP reporting
can connect from the Mercury host using a scoped database account. Desktop
workflows can use a dedicated Windows VM with the Mercury connector.

## Network file access (SMB)

SMB is an optional add-in that can be set up after the initial deployment.
If enabled, IT sets up the mount and manages its credentials. The file
server applies permissions to the identity used for the mount: the delegated
user or an account limited to their approved files. Mercury sign-in and
website Vault do not supply SMB credentials.

[Mercury overview](README.md) · [Identity, network access, and Vault](access-and-credentials.md)
