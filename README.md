# 📐 surveyor
Tools for surveying Dart packages

## Installing

These tools are best run from source.  To get the sources, clone the `suveyor` repo like this:

    $ git clone https://github.com/pq/surveyor.git

From there you can run the `examples`.

## Examples

### Surveying Widget Use

    dart bin/example/survey_widgets.dart <path_to_project>

will analyze the project at the given path and present a list of found `Widget` child-parent 2-Grams.

A sample run produces:

```
2 Grams:
Column->Container : 1
Column->null : 1
Container->Row : 1
Expanded->Column : 1
FlareActor->Container : 1
FlareActor->GestureDetector : 1
FlareActor->Scaffold : 1
GestureDetector->Expanded : 1
HomePage->null : 1
MaterialApp->null : 1
PageView->Scaffold : 1
Row->GestureDetector : 1
Scaffold->Column : 1
Text->Column : 5
```

(Note that by default package dependencies will only be installed if a `.packages` file is absent from the project under analysis.  If you want to make sure package dependencies are (re)installed, run with the `--force-install` option.)


## Features and bugs

This is very much a work in progress.  Please file feature requests, bugs and any feedback in the [issue tracker][tracker].

Thanks!

[tracker]: https://github.com/pq/surveyor/issues
