## Smooth

Create a line chart with gently curved lines instead of sharp angles.

### Example

```html
<div class="uk-chart-container max-w-md">
  <div class="p-4">
    <div class="uk-card-title">Line Chart - Smooth</div>
    <div class="uk-text-sm mt-2">January - June 2024</div>
  </div>

  <div class="px-4">
    <uk-chart>
      <script type="application/json">
        {
          "series": [
            {
              "name": "Desktops",
              "data": [186, 305, 237, 73, 209, 214]
            }
          ],
          "chart": {
            "type": "line",
            "zoom": {
              "enabled": false
            },
            "toolbar": {
              "show": false
            }
          },
          "dataLabels": {
            "enabled": false
          },
          "stroke": {
            "curve": "smooth",
            "width": 2
          },
          "colors": ["hsl(var(--chart-1))"],
          "grid": {
            "row": {
              "colors": []
            },
            "borderColor": "hsl(var(--border))"
          },
          "xaxis": {
            "categories": ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
            "tooltip": {
              "enabled": false
            },
            "labels": {
              "style": {
                "colors": "hsl(var(--muted-foreground))"
              }
            },
            "axisBorder": {
              "show": false
            },
            "axisTicks": {
              "show": false
            }
          },
          "yaxis": {
            "labels": {
              "show": false
            }
          },
          "tooltip": {
            "title": {
              "show": false
            }
          }
        }
      </script>
    </uk-chart>
  </div>

  <div class="p-4">
    <div class="flex items-center gap-x-2 font-medium leading-none">
      Trending up by 5.2% this month
      <uk-icon icon="trending-up"></uk-icon>
    </div>
    <div class="text-muted-foreground mt-2 leading-none">
      Showing total visitors for the last 6 months
    </div>
  </div>
</div>
```

## Straight

Creates a line chart with straight, angular connections between data points.

### Example

```html
<div class="uk-chart-container max-w-md">
  <div class="p-4">
    <div class="uk-card-title">Line Chart - Straight</div>
    <div class="uk-text-sm mt-2">January - June 2024</div>
  </div>

  <div class="px-4">
    <uk-chart>
      <script type="application/json">
        {
          "series": [
            {
              "name": "Desktops",
              "data": [186, 305, 237, 73, 209, 214]
            }
          ],
          "chart": {
            "type": "line",
            "zoom": {
              "enabled": false
            },
            "toolbar": {
              "show": false
            }
          },
          "dataLabels": {
            "enabled": false
          },
          "stroke": {
            "curve": "straight",
            "width": 2
          },
          "colors": ["hsl(var(--chart-1))"],
          "grid": {
            "row": {
              "colors": []
            },
            "borderColor": "hsl(var(--border))"
          },
          "xaxis": {
            "categories": ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
            "tooltip": {
              "enabled": false
            },
            "labels": {
              "style": {
                "colors": "hsl(var(--muted-foreground))"
              }
            },
            "axisBorder": {
              "show": false
            },
            "axisTicks": {
              "show": false
            }
          },
          "yaxis": {
            "labels": {
              "show": false
            }
          },
          "tooltip": {
            "title": {
              "show": false
            }
          }
        }
      </script>
    </uk-chart>
  </div>

  <div class="p-4">
    <div class="flex items-center gap-x-2 font-medium leading-none">
      Trending up by 5.2% this month
      <uk-icon icon="trending-up"></uk-icon>
    </div>
    <div class="text-muted-foreground mt-2 leading-none">
      Showing total visitors for the last 6 months
    </div>
  </div>
</div>
```

## Stepline

Creates a line chart with step-like connections between points.

### Example

```html
<div class="uk-chart-container max-w-md">
  <div class="p-4">
    <div class="uk-card-title">Line Chart - Stepline</div>
    <div class="uk-text-sm mt-2">January - June 2024</div>
  </div>

  <div class="px-4">
    <uk-chart>
      <script type="application/json">
        {
          "series": [
            {
              "name": "Desktops",
              "data": [186, 305, 237, 73, 209, 214]
            }
          ],
          "chart": {
            "type": "line",
            "zoom": {
              "enabled": false
            },
            "toolbar": {
              "show": false
            }
          },
          "dataLabels": {
            "enabled": false
          },
          "stroke": {
            "curve": "stepline",
            "width": 2
          },
          "colors": ["hsl(var(--chart-1))"],
          "grid": {
            "row": {
              "colors": []
            },
            "borderColor": "hsl(var(--border))"
          },
          "xaxis": {
            "categories": ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
            "tooltip": {
              "enabled": false
            },
            "labels": {
              "style": {
                "colors": "hsl(var(--muted-foreground))"
              }
            },
            "axisBorder": {
              "show": false
            },
            "axisTicks": {
              "show": false
            }
          },
          "yaxis": {
            "labels": {
              "show": false
            }
          },
          "tooltip": {
            "title": {
              "show": false
            }
          },
          "markers": {
            "hover": {
              "sizeOffset": 4
            }
          }
        }
      </script>
    </uk-chart>
  </div>

  <div class="p-4">
    <div class="flex items-center gap-x-2 font-medium leading-none">
      Trending up by 5.2% this month
      <uk-icon icon="trending-up"></uk-icon>
    </div>
    <div class="text-muted-foreground mt-2 leading-none">
      Showing total visitors for the last 6 months
    </div>
  </div>
</div>
```

## Multiple

Displays multiple lines on the same chart to compare different data series.

### Example

```html
<div class="uk-chart-container max-w-md">
  <div class="p-4">
    <div class="uk-card-title">Line Chart - Multiple</div>
    <div class="uk-text-sm mt-2">January - June 2024</div>
  </div>

  <div class="px-4">
    <uk-chart>
      <script type="application/json">
        {
          "series": [
            {
              "name": "Desktops",
              "data": [186, 305, 237, 73, 209, 214]
            },
            {
              "name": "Mobile",
              "data": [80, 200, 120, 190, 130, 140]
            }
          ],
          "chart": {
            "type": "line",
            "zoom": {
              "enabled": false
            },
            "toolbar": {
              "show": false
            }
          },
          "dataLabels": {
            "enabled": false
          },
          "stroke": {
            "curve": "smooth",
            "width": 2
          },
          "colors": ["hsl(var(--chart-1))", "hsl(var(--chart-2))"],
          "grid": {
            "row": {
              "colors": []
            },
            "borderColor": "hsl(var(--border))"
          },
          "xaxis": {
            "categories": ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
            "tooltip": {
              "enabled": false
            },
            "labels": {
              "style": {
                "colors": "hsl(var(--muted-foreground))"
              }
            },
            "axisBorder": {
              "show": false
            },
            "axisTicks": {
              "show": false
            }
          },
          "yaxis": {
            "labels": {
              "show": false
            }
          },
          "tooltip": {
            "title": {
              "show": false
            },
            "style": {
              "fontFamily": "inherit",
              "fontSize": "var(--uk-global-font-size-s)",
              "lineHeight": "var(--uk-global-line-height-s)"
            }
          },
          "legend": {
            "fontFamily": "inherit",
            "fontSize": "",
            "lineHeight": "",
            "markers": {
              "strokeWidth": 0
            }
          }
        }
      </script>
    </uk-chart>
  </div>

  <div class="p-4">
    <div class="flex items-center gap-x-2 font-medium leading-none">
      Trending up by 5.2% this month
      <uk-icon icon="trending-up"></uk-icon>
    </div>
    <div class="text-muted-foreground mt-2 leading-none">
      Showing total visitors for the last 6 months
    </div>
  </div>
</div>
```
