# udemy-dl
**A cross-platform python based utility to download courses from udemy for personal offline use.**

## ***Usage***

***Download a course***

    python udemy-dl.py COURSE_URL

***Download a courses from file***

    python udemy-dl.py FILE-CONTAINING-COURSE-URLs
  
***Download course with specific resolution***

    python udemy-dl.py COURSE_URL -q 720
  
***Download course to a specific location***

    python udemy-dl.py COURSE_URL -o "/path/to/directory/"
  
***Download course with specific resolution to a specific location***

    python udemy-dl.py COURSE_URL -q 720 -o "/path/to/directory/"

***Download specific chapter from a course***

    python udemy-dl.py COURSE_URL -c NUMBER

***Download specific lecture from a chapter***

    python udemy-dl.py COURSE_URL -c NUMBER -l NUMBER

***Download lecture(s) range from a specific chapter***

    python udemy-dl.py COURSE_URL -c NUMBER --lecture-start NUMBER --lecture-end NUMBER

***Download chapter(s) range from a course***

    python udemy-dl.py COURSE_URL --chapter-start NUMBER --chapter-end NUMBER

***Download specific lecture from chapter(s) range***

    python udemy-dl.py COURSE_URL --chapter-start NUMBER --chapter-end NUMBER --lecture NUMBER

***Download lecture(s) range from chapter(s) range***

    python udemy-dl.py COURSE_URL --chapter-start NUMBER --chapter-end NUMBER --lecture-start NUMBER --lecture-end NUMBER

***List down specific chapter from a course***

    python udemy-dl.py COURSE_URL -c NUMBER --info

***List down specific lecture from a chapter***

    python udemy-dl.py COURSE_URL -c NUMBER -l NUMBER --info

***Download specific subtite by using language code such as (en, es) if lang switch is not specified then default will be all subtitles***

    python udemy-dl.py COURSE_URL --sub-lang en


## **Advanced Usage**

<pre><code>
usage: udemy-dl.py [-h] [-v] [-u] [-p] [-k] [-o] [-q] [-c] [-l] [-s] [--chapter-start] [--chapter-end] [--lecture-start] [--lecture-end] [--info]
                   [--keep-vtt] [--sub-only] [--skip-sub] [--skip-hls] [--assets-only] [--skip-assets]
                   course

A cross-platform python based utility to download courses from udemy for personal offline use.

positional arguments:
  course            Udemy course.

General:
  -h, --help        Shows the help.
  -v, --version     Shows the version.

Authentication:
  -u , --username   Username in udemy.
  -p , --password   Password of your account.
  -k , --cookies    Cookies to authenticate with.

Advance:
  -o , --output     Download to specific directory.
  -q , --quality    Download specific video quality.
  -c , --chapter    Download specific chapter from course.
  -l , --lecture    Download specific lecture from chapter(s).
  -s , --sub-lang   Download specific subtitle/caption (e.g:- en).
  --chapter-start   Download from specific position within course.
  --chapter-end     Download till specific position within course.
  --lecture-start   Download from specific position within chapter(s).
  --lecture-end     Download till specific position within chapter(s).

Others:
  --info            List all lectures with available resolution.
  --keep-vtt        Keep WebVTT caption(s).
  --sub-only        Download captions/subtitle only.
  --skip-sub        Download course but skip captions/subtitle.
  --skip-hls        Download course but skip hls streams. (fast fetching).
  --assets-only     Download asset(s) only.
  --skip-assets     Download course but skip asset(s).

Example:
  python udemy-dl.py  COURSE_URL
  python udemy-dl.py  COURSE_URL -k cookies.txt
  python udemy-dl.py -u user@domain.com -p p4ssw0rd COURSE_URL
</code></pre>