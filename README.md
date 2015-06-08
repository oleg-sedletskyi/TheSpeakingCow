# TheSpeakingCow

A configurable speaking cow:

Cowsay generates an ASCII picture of a cow saying something provided by the user.  If run with no arguments, 
it accepts standard input, word-wraps the message given at about 40 columns, and prints the cow saying the 
given message on standard output.

To aid in the use of arbitrary messages with arbitrary whitespace, use the -n option.  If it is specified, 
the given message  will  not be  word-wrapped. If -n is specified, there must not be any command-line arguments
left after all the switches have been processed.
For example:

$ cowsay -n
d d d d da s da sd a sd as da s da sd as da sd a sd as d a sda sd a sd asd as da s
 ____________________________________________________________________________________
< d d d d da s da sd a sd as da s da sd as da sd a sd as d a sda sd a sd asd as da s >
 ------------------------------------------------------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||


And without the -n switch:
$ cowsay
d d d d da s da sd a sd as da s da sd as da sd a sd as d a sda sd a sd asd as da s
 _________________________________________
/ d d d d da s da sd a sd as da s da sd   \
| as da sd a sd as d a sda sd a sd asd as |
\ da s                                    /
 -----------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||



The -W specifies **roughly** where the message should be wrapped. The default is equivalent to -W 40 i.e.
wrap words at or before the 40th column.

If  any  command-line  arguments are left over after all switches have been processed,
they become the cow's message.  The program will not accept standard input for a message in this case.

There are several provided modes which change the appearance of the cow depending on its particular
emotional/physical state:

-b option initiates Borg mode:

$ cowsay -b Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (==)\_______
            (__)\       )\/\
                ||----w |
                ||     ||




-d causes the cow to appear dead:

$ cowsay -d Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (xx)\_______
            (__)\       )\/\
             U  ||----w |
                ||     ||




-g invokes greedy mode:

$ cowsay -g Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  ($$)\_______
            (__)\       )\/\
                ||----w |
                ||     ||




-p causes a state of paranoia to come over the cow:

$ cowsay -p Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (@@)\_______
            (__)\       )\/\
                ||----w |
                ||     ||




-s makes the cow appear thoroughly stoned:

$ cowsay -s Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (**)\_______
            (__)\       )\/\
             U  ||----w |
                ||     ||






-t yields a tired cow:

$ cowsay -t Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (--)\_______
            (__)\       )\/\
                ||----w |
                ||     ||




-w is somewhat the opposite of -t, and initiates wired mode:

$ cowsay -w Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (OO)\_______
            (__)\       )\/\
                ||----w |
                ||     ||



-y brings on the cow's youthful appearance:

$ cowsay -y Abracadabra
 _____________
< Abracadabra >
 -------------
        \   ^__^
         \  (..)\_______
            (__)\       )\/\
                ||----w |
                ||     ||






The  user  may specify the -e option to select the appearance of the cow's eyes (cowsay -e eye_string)
in which case the first two characters of the argument string eye_string will be used. 
The default eyes are 'oo'.

$ cowsay -e oO
What?!
 ________
< What?! >
 --------
        \   ^__^
         \  (oO)\_______
            (__)\       )\/\
                ||----w |
                ||     ||



$ cowsay Hello World!
 ______________
< Hello World! >
 --------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||


$ fortune | cowsay
 _______________________________________
/ I always wake up at the crack of ice. \
|                                       |
\ -- Joe E. Lewis                       /
 ---------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||



$ cowsay aksjdhkljsdahflkajshflkajshdfklajshdfklajshdflkajsdhflkjashdfkljasdhfaklsjdhfalksjd
 _________________________________________
/ aksjdhkljsdahflkajshflkajshdfklajshdfkl \
| ajshdflkajsdhflkjashdfkljasdhfaklsjdhfa |
\ lksjd                                   /
 -----------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||






Create another program: cowthink. It is the same program as before, but the cow will think its message instead of saying it:

$ fortune computers | cowthink -p
 _________________________________________
( I wish you humans would leave me alone. )
 -----------------------------------------
        o   ^__^
         o  (@@)\_______
            (__)\       )\/\
                ||----w |
                ||     ||


$ fortune startrek | cowthink -p
 _________________________________________
( Extreme feminine beauty is always       )
( disturbing.                             )
(                                         )
( -- Spock, "The Cloud Minders", stardate )
( 5818.4                                  )
 -----------------------------------------
        o   ^__^
         o  (@@)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
                

This program should use the same library(-ies) as the first one and should reuse as much as possible (NO COPY PASTE!).
Both programs should be short. Most of the code should be in reusable library(-ies).
Programs should only consist of logic specific for thinking/speaking cow.

You should think in terms of objects (classes).
