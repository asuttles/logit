# LOGIT

A simple command-line utility written in Perl that logs simple daily activities and metrics.

## Features

* Quickly add items to a csv log
* Generate simple reports for a time-limited period

## Requirements

* Time::Piece;
* Getopt::Long;
* Text::CSV;

### FreeBSD

Install required packages:

```sh
pkg install p5-Time-Piece
pkg install p5-Getopt-Long
pkg install p5-Text-CSV
```

## Installation

Clone the repository:

```sh
git clone https://github.com/asuttles/logit.git
cd logit
```

Make the script executable:

```sh
chmod +x logit
```

## Usage

Add a daily run to the log:
```sh
./logit add run 30 minutes
```

Add a daily weigh-in to the log:
```sh
./logit add weight 175 pounds
```

Print a report of all banjo sessions:
```sh
./logit report banjo
```

Print a report of systolic blood pressure readings over the past 20 days:
```sh
./logit report systolic --last 20
```

Print a report of pushups with a summary:
```sh
./logit report pushups --summary
```

Display help:

```sh
./logit help
```

## License

This project is licensed under the BSD 2-Clause License. See the LICENSE file for details.
