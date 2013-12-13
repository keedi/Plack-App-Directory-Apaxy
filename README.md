# NAME

Plack::App::Directory::Apaxy - Serve static files from document root with directory index using Apaxy

# VERSION

version 0.004

# SYNOPSIS

    # app.psgi
    use Plack::App::Directory::Apaxy;
    my $app = Plack::App::Directory->new({ root => "/path/to/htdocs" })->to_app;

    # one-liner
    $ plackup -MPlack::App::Directory::Apaxy -e 'Plack::App::Directory::Apaxy->new->to_app'

    # one-liner using Starlet
    $ plackup -s Starlet -MPlack::App::Directory::Apaxy --max-workers=5 -e 'Plack::App::Directory::Apaxy->new->to_app'

# DESCRIPTION

This is a static file server PSGI application with directory index using Apaxy.

# ATTRIBUTES

## root

Document root directory. Defaults to the current directory.

## apaxy\_root

Apaxy resource root directory. Usually you don't need to set it up by your hand.

## below

HTML contents what you want to insert to index page.

## footer

HTML contents what you want to insert to index page.

# SEE ALSO

- [Plack::App::Directory](https://metacpan.org/pod/Plack::App::Directory)
- [Apaxy](http://adamwhitcroft.com/apaxy/)

# AUTHOR

Keedi Kim - 김도형 <keedi@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2013 by Keedi Kim.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
