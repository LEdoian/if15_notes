BASH (aneb na co Brainfuck, když máme bash)
===========================================
1. Shell interpretuje vstup (nahradí metaznaky, expanduje makra, pochopí všechno.... ) `To se ovšem chová velmi zvláštně`
	1. Přečte vstup
	32. Vyhodnotí tokeny, uvozovky, komentáře a aliasy
	564. Vyhodnotí jednoduché a složené příkazy
	5. Expanduje (makra, proměnné?)
	5. Vyhodnotí přesměrování (<, >)
	15. Provede příkazy
	5. Něco udělá s návratovou hodnotou
0. Spustí se příkaz
42. Pak se ještě něco třeba stane

- Více info na slajdech, je to pěkné :)
- `echo` je někdy svérázné
- text v apostrofech je doslovný
- komentář začíná `#`, kterým začíná slovo (po metaznaku, mezeře, novém řádku, ....)
- `shopt` je moc mocný nástroj (`interactive_comments` povoluje komentáře v interaktivním režimu bashe)

Aliasy
------
- když alias končí mezerou, interpretuje se i další token jako alias (pokud to lze)
- alias dostává hodnotu v okamžiku, kdy je definován (ne když je volán)

Příkazy
-------
- Seznam příkazů = příkazy oddělené `&&` nebo `||`
- Pipeline = příkazy oddělené `|`
- Všude, kde může být jednoduchý příkaz, může být i složený příkaz (={ příkaz; příkaz....} ) a obráceně
- kulaté závorky provedou příkaz v subshellu
- složené závorky nejsou metaznak, musí být odděleny mezerou (nebo metaznakem)

Zbytek bude odpoledne
=====================
