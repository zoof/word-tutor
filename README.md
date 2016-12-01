# Word Tutor

A very basic Python 2.7 script (command line terminal) that:
 1. reads in a list of words
 2. randomized them
 3. asks the student to spell each word with the option to repeat the word or to give up
 4. upon completion of each word, the definition is printed out.

There are two APIs being used to drive this. The first is Amazon's Ivona service for the text to speech (`ivona_api`).  The second is wordnik to look up definitions (`wordnik`). Access to these APIs requires registering with each service to get access keys which are put into a file `secret.yaml`.  This file takes the following form:

    ivona-access-key: <IVONA ACCESS KEY>
    ivona-secret-key: <IVONA SECRET KEY>
    wordnik-key: <WORDNIK KEY>

In additional, the script requires `python-vlc` to play the audio (and hence vlc must also be installed) and `pyyaml` to read the authentication keys. In an Anaconda installation, this can be done by

    $ conda install cryptography
    $ pip install ivona_api
    $ pip install wordnik
    $ pip install python-vlc
