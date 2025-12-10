tequ-node-red-plotly-trace
=====================

Format Plotly trace

## Install

Run the following command in your Node-RED user directory - typically `~/.node-red`

        npm install tequ-node-red-plotly-trace

## Information

Create Plotly trace.

Output should be forwarded to "add"-node and optionally to "memory"-node.

Usage of this node requires more or less knowledge about [Plotly.js](https://plotly.com/javascript/configuration-options/) library.

By default expects following input message:

`{
    "payload":11.45,
    "timestamp":"2025-10-10T00:00:00Z"
}`

Parameters can be set in input message:

 - payload = msg.payload (number, value that is added to chart)
 - timestamp = msg.timestamp (timestamp, if pre-formatted use Plotly format YYYY-MM-DD HH:mm:ss.SSS)
 - Type = msg.chart_type ("scatter" | "bar")
 - Mode = msg.chart_mode ("lines" | "lines+markers" | "markers")
 - Chart name = msg.chart_name (string)
 - History size = msg.chart_history_size (number)
 - Line = msg.trace_parameters (JSON, Plotly format)
- Marker = msg.marker_parameters (JSON, Plotly format)
- Trace name = msg.topic (string)
- Time format = msg.format_ts (1 | 2 | 3 | 4 )
- Show status = msg.show_status (true | false)
- Buffer size = msg.buffer_size (number)
- Input timezone = msg.in_tz (Timezone string)
- Output timezone = msg.out_tz (Timezone string)
- Y axis = msg.y_axis ("y1" | "y2")
- Hover template = msg.hover_template (Plotly format string)
- Action = msg.action ("update_data" | "add_data" )

If using buffering, time format should be set to "3 = Do not format timestamp".
