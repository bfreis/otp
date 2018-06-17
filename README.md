# otp - One Time Password generation with Bash

This script generates Hash-based One Time Passwords (HOTP) and Time-based One Time Passwords (TOTP).

It's written in bash, and has a minimal set of dependencies.

HMACs are calculated with OpenSSL, and date/string manipulation is done with GNU coreutils.

## Installation

To install, simply put the `otp` script in your `$PATH`.

Make sure to install the required dependencies. This has been tested with dependencies installed by Homebrew on Mac and Linuxbrew on Amazon Linux.

After installing Homebrew or Linuxbrew, simply run:

    brew install coreutils openssl bash

## Status and roadmap

Currently, this script simply implements the algorithms and passes all the test cases defined in the specifications.

The goal is to allow the generation of HOTP and TOTP based on secret-specification parameters passed either through cmd line arguments or stdin.

The stdin use case is intended to allow easy integration with command-line based secret storage, such as https://www.passwordstore.org/, or https://github.com/lastpass/lastpass-cli.

## Specs

- HOTP: https://tools.ietf.org/html/rfc4226

- TOTP: https://tools.ietf.org/html/rfc6238



