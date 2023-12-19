# vim:ft=python:

genrule(
    name = 'version',
    out = 'version.json',
    bash = r"""echo "{\"revision\": \"`git rev-parse HEAD`\"}" > $OUT""",
)

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
    resources = [
        ':version',
    ],
)

python_binary(
    name='result',
    main_module='main',
    deps=[
        ':main.lib',
    ]
)
