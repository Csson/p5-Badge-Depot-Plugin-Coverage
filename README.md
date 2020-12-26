# NAME

Badge::Depot::Plugin::Coverage - Code coverage plugin for Badge::Depot

# VERSION

Version 0.0102, released 2020-12-26.

# SYNOPSIS

Used standalone:

    use Badge::Depot::Plugin::Coverage;

    my $badge = Badge::Depot::Plugin::Coverage->new(coverage => 87);

    print $badge->to_html;

Used together with [Pod::Weaver::Section::Badges](https://metacpan.org/pod/Pod::Weaver::Section::Badges), in weaver.ini:

    [Badges]
    ; other settings
    badge = Coverage

# DESCRIPTION

This [Badge::Depot](https://metacpan.org/pod/Badge::Depot) badge is meant to be used together with [Dist::Zilla::App::Command::coverh](https://metacpan.org/pod/Dist::Zilla::App::Command::coverh) (or standalone, as per the synopsis) and creates a coverage badge:

![Coverage 87%](https://img.shields.io/badge/coverage-87%25-orange.svg)

# ATTRIBUTES

## coverage

Set the code coverage percentage manually. Should only be used when [Dist::Zilla::App::Command::coverh](https://metacpan.org/pod/Dist::Zilla::App::Command::coverh) is **not** used.

## custom\_image\_url

Default: `https://img.shields.io/badge/%s-%s-%s.svg`

Override the default image url. It is expected to have three `sprintf` placeholders: Text, coverage percentage and color.

## max\_age

Default: `60`

When used together with [Dist::Zilla::App::Command::coverh](https://metacpan.org/pod/Dist::Zilla::App::Command::coverh), only include the badge if the latest coverage run was less than `max_age` minutes ago.

## text

Default: `coverage`

Set a different coverage percentage. The percentage sign will be appended.

# SEE ALSO

- [Badge::Depot](https://metacpan.org/pod/Badge::Depot)
- [Task::Badge::Depot](https://metacpan.org/pod/Task::Badge::Depot)

# SOURCE

[https://github.com/Csson/p5-Badge-Depot-Plugin-Coverage](https://github.com/Csson/p5-Badge-Depot-Plugin-Coverage)

# HOMEPAGE

[https://metacpan.org/release/Badge-Depot-Plugin-Coverage](https://metacpan.org/release/Badge-Depot-Plugin-Coverage)

# AUTHOR

Erik Carlsson <info@code301.com>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2016 by Erik Carlsson.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
