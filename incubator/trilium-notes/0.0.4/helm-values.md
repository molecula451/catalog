# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.TRILIUM_DATA_DIR | string | `"/trilium-data"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/trilium-notes"` |  |
| image.tag | string | `"v0.49.5@sha256:32262e0829730850f83f5e0227ff83cd5c9cc443aeacb461daf1cec7b710259e"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/trilium-data"` |  |
| service.main.ports.main.port | int | `10086` |  |
| service.main.ports.main.protocol | string | `"HTTP"` |  |
| service.main.ports.main.targetPort | int | `8080` |  |

All Rights Reserved - The TrueCharts Project