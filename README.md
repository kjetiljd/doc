# NAIS

## What is NAIS?

NAIS is an open source application platform that aims to provide our developers with the best possible tools needed to develop and run their applications.

## Why NAIS exists

When you have a large development organisation, providing the developers with turnkey solutions for their most common needs can be a good investment.

This includes \(but not limited to\) [logging](https://github.com/nais/doc/tree/ed810945684e0f22aaeec0662a28da7a397f6b67/logging/README.md), [metrics](https://github.com/nais/doc/tree/ed810945684e0f22aaeec0662a28da7a397f6b67/metrics/README.md), [alerts](https://github.com/nais/doc/tree/ed810945684e0f22aaeec0662a28da7a397f6b67/alerts/README.md), [deployment](https://github.com/nais/doc/tree/ed810945684e0f22aaeec0662a28da7a397f6b67/deploy/README.md) and a [runtime environment](https://github.com/nais/doc/tree/ed810945684e0f22aaeec0662a28da7a397f6b67/clusters/README.md).

Within each of these aspects, we leverage open source projects best suited for our needs and provide them with usable abstractions, sane defaults and the required security hardening.

## NAIS clusters

NAIS is a platform spread over two different suppliers. One set of clusters on-premise, and another set running in the cloud \(namely Google Cloud Platform.

### On-premise

The on-premise clusters are split into two zones, _selvbetjeningsonen_ \(SBS\), \_fagsystemsonen\_ \(FSS\).

| ingresses |  |
| :--- | :--- |
| dev-fss | nais.preprod.local |
| prod-fss | nais.adeo.no |
| dev-sbs | nais.oera-q.no |
| prod-sbs | nais.oera.no, tjenester.nav.no |

Example: If your app is named `myapp`, then the URL for `dev-fss` would be `https://my-app.nais.preprod.local/`.

{% hint style="info" %}
Remember `https://` when calling on-premise URLs!
{% endhint %}

{% hint style="warning" %}
We are working on moving away from the `preprod` prefix, so use `dev` where possible. Read more about the decision over at [pig-kubernetes-ops](https://github.com/navikt/pig/blob/master/PIG-Kubernetes-OPS/adr/000-preprod-rename.md).
{% endhint %}

### Cloud/GCP

For the cloud there are no zones. Instead, we rely on a zero-trust model with a service-mesh.

| cluster | ingresses |
| :--- | :--- |
| dev-gcp | dev-adeo.no, dev-nais.no |
| prod-gcp | adeo.no |

## Contact the NAIS team

The team can be found either on [Slack](https://nav-it.slack.com/messages/C5KUST8N6/) or in Sannergata 2, 3nd floor west wing.

Also, follow us on Twitter [@nais\_io](https://twitter.com/nais_io)!

