Traceback (most recent call last):
  File "<string>", line 1, in <module>
    import pathlib,sys; sys.stdout.write(pathlib.Path('scripts/release-repository/README.md').read_text(encoding='utf-8'))
                        ~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\matth\AppData\Roaming\uv\python\cpython-3.13-windows-x86_64-none\Lib\encodings\cp1252.py", line 19, in encode
    return codecs.charmap_encode(input,self.errors,encoding_table)[0]
           ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
UnicodeEncodeError: 'charmap' codec can't encode character '\u2192' in position 883: character maps to <undefined>
