# csv2xlsx
A fork of cpan's Text::csv_xs  helpful little csv2xlsx example with a touch more documentation, by H. Merijn Brand (https://metacpan.org/release/Text-CSV_XS)

I've forked this entirely to just import multiple csv files into one xslx file as multiple sheets. Sheets are numbered sequentially, in the order given to the program. 

This is occasionally invaluable. 


```usage: csv2xlsx [-s <sep>] [-q <quot>] [-w <width>] [-d <dtfmt>]
               [-o <xlsx>] [file.csv]
       -s <sep>   use <sep>   as seperator char, auto-detect, default = ','
                  The string "tab" is allowed.
       -e <esc>   use <esc>   as escape    char, auto-detect, default = '"'
                  The string "undef" is allowed.
       -q <quot>  use <quot>  as quotation char,              default = '"'
                  The string "undef" will disable quotation.
       -w <width> use <width> as default minimum column width default = 4
       -o <xlsx>  write output to file named <xlsx>, defaults
                  to input file name with .csv replaced with .xlsx
                  if from standard input, defaults to csv2xlsx.xlsx
       -F         allow formula's. Otherwise fields starting with
                  an equal sign are forced to string
         --Fa=aaa Define formula action: die/croak/diag/empty/undef
         --Fd     Formula's will cause a die
         --Fc     Formula's will cause a croak
         --FD     Formula's will cause a warning (this is the default)
         --Fe     Formula's will be replaced by the empty string
         --Fu     Formula's will be replaced with an undefined cell
       -f         force usage of <xlsx> if already exists (unlink before use)
       -d <dtfmt> use <dtfmt> as date formats.   Default = 'dd-mm-yyyy'
       -C <C:fmt> use <fmt> as currency formats for currency <C>, no default
       -D cols    only convert dates in columns <cols>. Default is everywhere.
       -u         CSV is UTF8
       -m         merge multiple CSV's into a single xlsx (separate sheets)
                    -o is required, all arguments should be existing files
       -v [<lvl>] verbosity (default = 1)
```
Perl_5 license. 
