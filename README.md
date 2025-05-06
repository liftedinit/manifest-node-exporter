# Manifest Node Exporter

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/liftedinit/manifest-node-exporter/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/liftedinit/manifest-node-exporter/tree/main)

A Prometheus exporter for collecting metrics from Manifest blockchain nodes. The exporter is designed to automatically detect which services are running on the node and collect relevant metrics.

## Installation

Download the latest release from the [releases page](https://github.com/liftedinit/manifest-node-exporter/releases)

## Quick Start

```bash
manifest-node-exporter serve [flags]
```

The exporter will start a Prometheus metrics server on `0.0.0.0:2112` by default.

## Global Flags

| Flag                | Description                                                                               |
|---------------------|-------------------------------------------------------------------------------------------|
| `-h`, `--help`      | help for manifest-node-exporter                                                           |
| `-l`, `--logLevel` | Set the log level. Available levels: `debug`, `info`, `warn`, `error`. Default is `info`. |

## Serve Flags

| Flag                | Description                                                                               |
|---------------------|-------------------------------------------------------------------------------------------|
| `-h`, `--help`      | help for serve                                                                           |
| `--listen-address` | Address to listen on for Prometheus metrics. Default is `0.0.0.0:2112`.                |

## Metrics

| Metric Name                         | Description                                                               |
|-------------------------------------|---------------------------------------------------------------------------|
| `manifest_tokenomics_denom_info`    | Information about the token denominations (symbol, denom, name, display). |  
| `manifest_tokenomics_total_supply`  | Total supply for a given token.                                           |
| `manifest_tokenomics_token_count`   | The number of different tokens hosted on the Manifest blockchain.         |
| `manifest_tokenomics_denom_grpc_up` | Whether the gRPC query for the token denomination was successful.         |
| `manifest_tokenomics_count_grpc_up` | Whether the gRPC query for the token count was successful.                |
| `manifest_geo_info`                 | Node's geographical information (country, city, region, etc)              |
| `manifest_geo_latitude`             | Node's geographical latitude                                              |
| `manifest_geo_longitude`            | Node's geographical longitude                                             |