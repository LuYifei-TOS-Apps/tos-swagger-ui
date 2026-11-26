# Swagger UI on TOS privacy policy

This policy covers the self-hosted TOS package for Swagger UI. The NAS administrator operates the installation and controls its data and backups.

## Data and purpose

The server reads the operator's OpenAPI document from the directory mounted read-only at `/spec` or serves a local example. Anyone who can reach the UI can retrieve the served document. HTTP access logs can include addresses, paths and times.

## Sharing and external services

When users choose Try it out, their browsers send the request, parameters and any credentials they enter to the API server declared by the specification. The TOS recipe disables the remote Swagger validator. The configured API controls its own request and response retention.

Installation and updates can contact TOS distribution services and container registries to obtain packages and images. Requests to external services are handled according to the services and locations selected by the operator.

## Retention, access, correction and deletion

The specification remains until its owner edits or deletes it in the mounted directory. Its owner can replace it and recreate the container to serve the new version. The NAS administrator manages Docker logs and backups.

To remove an entire instance, stop it and identify the app-owned storage in Docker Manager before deleting it. The NAS administrator should handle retained backups separately and verify the effects of the TOS uninstall options. Contact the NAS administrator to request access, correction or deletion of data held by the instance.

## Security and support

Publish only specifications authorized for the intended audience. Restrict access to the port or use an authenticated TLS proxy for a private specification. Keep secrets out of example documents.

For questions about the TOS package, use the repository's issue tracker. Omit private data, credentials and unredacted logs from public reports.
