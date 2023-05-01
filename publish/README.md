# Notebook Publication

There are different ways to publish your notebooks,
choose one that best fits your concrete situation.
For example, publishing publically (on the internet) vs.
within an organization requires workflows fitting
the specific environment.


## Convert a Notebook to HTML

To create a self-contained HTML file (embedding all CSS, images, and so on), call the following command:

    jupyter nbconvert --execute --to html «NOTEBOOK».ipynb \
        && xdg-open ${_%.*}.html

The second command opens your browser with the result (on Linux).

Add the `-theme=dark` option to the `nbconvert` command to get a white-on-black rendering, except for your charts which will be rendered like you styled them.

Using `--no-input` hides *all* code cells and allows you to publish a more 'normal' report, where the way you created the result is of no interest and just those results should be visible.

You can then upload the HTML file to a place where your audience can conveniently retrieve or view it.
Within a company that can be a shared documentation space (Confluence, Sharepoint, …) or
a repository server that is able to serve HTML content (e.g. JFrog Artifactory).


## More Resources

* [Reporting Generation with Notebooks](https://anaconda.org/jbednar/reporting/notebook) – Part 2 of a 2017 Anaconda webinar on Python data visualization.
