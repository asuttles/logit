# LOGIT

A simple command-line utility written in Perl that logs simple daily activities and metrics.

## Features

* Quickly add items to a csv log from the terminal
* Generate simple terminal reports for a specified time period

## Requirements

* Time::Piece
* Getopt::Long
* Text::CSV

### Packages

To install required packages on FreeBSD:

```sh
sudo pkg install p5-Time-Piece
sudo pkg install p5-Getopt-Long
sudo pkg install p5-Text-CSV
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

Install it on the local system:
```sh
sudo install -m 755 ./logit /usr/local/bin/logit
```

## Usage

Add today's daily run to the log:
```sh
logit add today run 30 minutes
```

Add a weigh-in from a specific date to the log:
```sh
logit add 2015-07-04 weight 175 pounds
```

Print a report of all banjo sessions:
```sh
logit report banjo
```

Print a report of systolic BP readings over the last 20 days:
```sh
logit report systolic --last 20
```

Print a report of pushups with a summary:
```sh
logit report pushups --summary
```

Print the date intersection of 2+ categories:
```sh
logit intersect run pushups
```


Display help:

```sh
logit help
```

## License

This project is licensed under the BSD 2-Clause License. See the LICENSE file for details.
