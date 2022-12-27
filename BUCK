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
    main_module='main',
    deps=[
        ':main.lib',
    ]
)
