# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.PUID | int | `568` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/emulatorjs"` |  |
| image.tag | string | `"v1.4.2"` |  |
| persistence.data.enabled | bool | `true` |  |
| persistence.data.mountPath | string | `"/data"` |  |
| persistence.varrun.enabled | bool | `true` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.front.ports.front.port | int | `10124` |  |
| service.front.ports.front.targetPort | int | `80` |  |
| service.ipfs.ports.ipfs.port | int | `10138` |  |
| service.ipfs.ports.ipfs.targetPort | int | `4001` |  |
| service.main.ports.main.port | int | `10130` |  |
| service.main.ports.main.targetPort | int | `3000` |  |

All Rights Reserved - The TrueCharts Project