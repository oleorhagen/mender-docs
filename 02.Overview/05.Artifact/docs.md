---
title: Artifact
taxonomy:
    category: docs
---

NOTE: Also add relation to the release

A Mender Artifact is the custom file format which is used to package an update
along with the required meta-data which the Mender server and the Mender client
need. Artifacts can either be created locally through the [mender-artifact
tool](https://github.com/mendersoftware/mender-artifact). It is also possible to
have the Mender server create one for you by simply updating the file in the
[UI](https://hosted.mender.io).

The Mender Artifact handles security important issues such as cryptographic
verification and signing of the software update. It is flexible enough to handle
all the different update types supported by Mender, that is: rootfs-updates,
Docker containers, scripts, single-file updates, etc.

After an Artifact is uploaded to the Mender server, it can be added to a
deployment, and then distributed to the devices in question. The devices are
filtered depending on the meta-data present in the Artifact, such as current
software version, device type, and optionally custom meta-data added by you.

The [state-scripts](../08.State-scripts/docs.md) functionality is also a part of
an Artifact, and can add custom functionality to an update.
