### General notes

#### Curl

- curl is used in command lines or scripts to trasnfer data

  ```bash
    $ curl www.example.com -i
  ```

- This will download print the HTML and header response from an HTTP get request to www.example.com

  ```bash
    $ curl www.example.com > example.html
  ```

- This will download and store the output in a file

  - o (lowercase o) the result will be saved in the filename provided in the command line
  - O (uppercase O) the filename in the URL will be taken and it will be used as the filename to store the result

  ```bash
    $ curl -o mygettext.html http://www.gnu.org/software/gettext/manual/gettext.html

    $ curl -O http://www.gnu.org/software/gettext/manual/gettext.html
  ```

- Multiple Files can be downloaded in a single shot by specifying the URLS in the command line

  - Syntax for multiple downloads

  ```bash
    $ curl -O URL1 -O URL2
  ```

- We can allow curl to follow HTTP location headers with the -L option.

  ```bash
    $ curl -L http://www.google.com
  ```

- Using the curl -C option, you can resume a download that was stopped early. It's useful for downloading large files that get interrupted

  ```bash
  $ curl -O http://www.gnu.org/software/gettext/manual/gettext.html
  ##############             20.1%

    /// CRT+C to stop the download, and then resume it with the -C option

  curl -C - -O http://www.gnu.org/software/gettext/manual/gettext.html
  ###############            21.1%
  ```

- The Limit rate of a data transfer can be set with the --limit-rate option

  ```bash
    $ curl --limit-rate 1000B -O http://www.gnu.org/software/gettext/manual/gettext.html
  ```

- We can download files that are modified after a particular time using -z option

  ```bash
    $ curl -z 21-Dec-11 http://www.example.com/yy.html
  ```

- HTTP Authentication can be passed in curl aswell. This can be set with the -u option

  ```bash
    $ curl -u username:password URL
  ```
