﻿#Whitewidow SQL Vulnerability Scanner

#How it works
Place search parameters inside of search_query.txt inside of lib folder

Once you have search parameters, whitewidow will use the parameters as a google search and return the first page;
(second page coming soon) of the google search.

From there whitewidow will pull the URLs from the first page of google and save them into a temporary log file under
/tmp/SQL_sites_to_check.txt.

Whitewidow will read this file and begin a vulnerability check on the webpages by adding an apostrophe to the end of
the URL.

If the URL produces a SQL syntax error the URL is saved into a temporary log file under /tmp/SQL_VULN.txt, if the URL
produces any type of error, 404, 401, 503, etc.. The URL will be saved into a log file under /log/non_exploitable.txt.

After the program has run it's search queries, the temporary SQL_VULN.txt is copied over to /log/SQL_VULN.LOG and is
truncated for further searches.

#Demo
whitewidow.rb

    ( W ( h ( i ( t ( e ( w ( i ( d ( o ( w )
               ( S ( Q ( L )
             ( V ( u ( l ( n )
        ( S ( c ( a ( n ( n ( e ( r )

                   _\{"}/_
                    //^\\


    Credits to my creator: Ekultek, he's a beast!
    I am currently version: '1.0.1', stick around for upgrades!
    My name is: Whitewidow, that's right albino widow

         [ LEGAL DISCLAIMER ]

         I was written as a learning tool only, also
         I should be treated as such. My purpose is
         to teach you what a SQL vulnerable website looks
         like, and to teach you how to prevent yourself
         from becoming vulnerable.

         Please ensure to inform all owners of vulnerable
         websites found while running me. My owner claims
         no responsibilities for any malicious actions
         taken with the information that is discovered
         while running me.

         Thank you for reading through my disclaimer and remember
         to provide all information to the owners of the sites
         All the information that I consider important will be
         stored in my log files.
         _________________________________________________________________

         [ TERMS OF SERVICE ]

         And now a note from my creator, the floor is all yours!

         Thank you by continuing with the processes of this program you
         agree, that all info discovered will be reported immediatly to
         the owners of the web pages.

         Furthermore you agree that the owner and writer of this program,
         is not responsible for the actions taken upon the knowledge gained
         from use of this program.

         Please take the time to read through the Legal Disclaimer and the
         Terms of Service.

         If for any reason you do not agree with the disclaimer, or terms,
         please exit this program immediatly.


         Press enter to continue...


     [23:30:24 INFO]I'll run in default mode then!

     [23:30:24 INFO]I'm searching for possible SQL vulnerable sites, using search query inurl:product-item.php?id=

     [23:30:25 SUCCESS]Site found: http://statelinefurniture.com.au/product-item.php?item=

     [23:30:26 SUCCESS]Site found: http://www.prosupps.co.za/product-item.php?id=6

     [23:30:27 SUCCESS]Site found: http://www.tamiyausa.com/product/item.php?product-id=53937

     [23:30:28 SUCCESS]Site found: https://www.tamiyausa.com/product/item.php?product-id=58395

     [23:30:29 SUCCESS]Site found: http://www.ozscopes.com.au/catalogsearch/result/?q=motor+drive+for+saxon+f1149eq%2F%2Fprod
     uct-item.php%3Fid%3D''%22+and+%22x%22%3D%22x+and+1%3D1--+allinurl%3Ainurl%3Aproduct-item.php%3Fid%3D''+UNION+ALL+SELE

     [23:30:30 SUCCESS]Site found: http://www.ozscopes.com.au/catalogsearch/result/?q=motor+drive+for+saxon+f1149eq%2Fproduct
     -item.php%3Fid%3D%22+and+%22x%22%3D%22x+and+1%3D1--)+ORDER+BY+2)+ORDER+BY+3+LIMIT+0+1+UNION+ALL+SELECT+N+An

     [23:30:31 SUCCESS]Site found: http://www.zoodigitalpublishing.com/product-item.php?id=291

     [23:30:32 SUCCESS]Site found: http://jobs.visa.com/search/inurl-product-item-php-id.html?q=inurl-product-item-php-id&q2=
     &locationsearch=

    [23:30:33 SUCCESS]Site found: https://jobs.visa.com/search/inurl-product-item-php-id-jobs.html?q=inurl-product-item-php-
    id-jobs

    [23:30:34 SUCCESS]Site found: http://www.docs-engine.com/pdf/1/product-item-php-id.html

#Help
Push, pull, fork, whatever you want to do, if you wanna help it would be great!

