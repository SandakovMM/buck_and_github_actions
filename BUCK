# Copyright 1999-2022. Plesk International GmbH. All rights reserved.
# vim:ft=python:

python_library(
    name='library.lib',
    srcs=[
        './library/__init__.py',
        './library/main.py',
    ]
)

python_library(
    name='main.lib',
    srcs=['main.py'],
    deps=[
        ':library.lib',
    ],
)

python_binary(
    name='result',
    platform='py3',
    main_module='main',
    deps=[
        ':main.lib',
    ]
)
