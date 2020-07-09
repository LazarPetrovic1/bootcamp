1. Kako se ispituju pravila (Odgovor: uslov po uslov sve dok se ispunjavaju uslovi)
2. Kad si u offense-u kako mozes doci do event-a i flow-a (odgovor: Kliknes na broj generisanih event-a/flow-a ili kliknes na ikonu event-a/flow-a)
3. Gde moze da se podesi da se uradi annotiation - u offense details
4. Tebi se nekom adminu poslalo 15 mail-a u 10 minuta, kako to da sprecis? - response limiter (1 mail/1 hr/ 1 custom property)
5. Stateless vs Statefull rules (Ne secam se pitanja, pogledajte) - pass
6. Kad saljes mail kakav treba da bude naslov mail-a (ili sadrzaj) - pass
7. User guide (strana 56. odgovor 2010-000 je odgovor, ako vam se javi pitanje) - neki specifican search
8. Sending email notifications (strana 47., imate podvuceno sta treba da zapamtite)
9. Ako dodje neki event koji je vezan za offense koji postoji (ali on je inactive), sta se desava sa eventom - novi offense
10. Sta se desava kad prodje retention period od offense-a - brise se ako nije protected
11. Zasto se offense nije obrisao posle retention period-a - proteceted je
12. Gde se nalazi Vulnerabilites (U Asset)
13. Super flow types (Type B - DDOS)
14. Anomaly detection rules
15. Confidence factor
16. Kako doci do base 64 payload-a - putanja - offense summary > payload information (biras izmedju UTF-8, Hex i Base64)
17. Log source time, start time, storage time itd. (timestamp) - verovatno log source; ako ima u pitanju `event pipeline`, onda je storage time, else start time
18. AQL pitanja (bilo ih je 3, pogledajte sintaksu i odakle se izvlace eventi, flow i sl)
19. Kad ce da se opet reavaluate magnitude offens-a? - kad mu se pripoji novi event sa svojim relevance, credibility i severity vrednostima (valjda)
20. Time series graph (definicija) - pass
21. Koji se grafovi koriste u reportovima - line, stacked line, bar, stacked bar, horizontal bar, pie, table, aggregate table
22. Reportovi (Ako si dao schedule report svakog ponedeljka i svakog prvog u mesecu, a zatrazis u cetvrtak report, sta ce da ti vrati?) - whole week
23. Ako hoces da vratis antivirus logove... - izaberes, tipa McAffee...
24. Za admin tab gde se nalazi network hierarchy - pass
25. Indexed Managment, Database managment itd... (Pogledajte sta sta znaci)
26. Gde se eventi cuvaju u arhitekturi (ponudjeno event processor, flow processor, event collector i nesto sto nema veze sa zivotom) (event processor) - Google kaze u konzoli (?)
27. SAR Threshold crossed (pogledajte na google) - Google kaze sledece: It has been identified that QRadar can report "SAR Sentinel: Threshold crossed for drbd0" system notifications for managed hosts in a High Availability (HA) pair. Investigation has determined that these messages can be excessively and erroneously generated due to a change made within the fix for APAR IJ06526.
28. Showing hidden offenses - offense tab (add notes && show hidden offenses)
29. Sta ima flow a nema event (bytes i packets)
30. Sta treba uraditi da se dashboard item deli sa svim korisnicima - QRadar: Sharing Dashboards Items. Create and share the Search Criteria, that the Dashboard Item will use. Have Users modify the shared Search Criteria for use on their Dashboards. Have Users add the shared Search Criteria as a Dashboard Item.
31. DSSE (Device stop sending events) - runs in the absence of events
32. Wizard uses the following key elements to create reports (layout, container, content)
33. Offense (Magnitude) - znajte sta je, bilo je navedeno kao odgovor (weighted mean of relevance, credibility & severity)
34. Bilo je pitanje kad radis pretragu po custom proprety i ne vidi se rezultat sta se desilo (odgovor - nije nasao nista za taj custom proprety, tipa url si stavio da trazi, ali u eventu nemas url)
35. Coalesing events (pogledajte sta je i kako funkcionise, bilo je pitanje za to) - Event coalescing starts after three events have been found with matching properties within a 10 second period. Event Coalescing helps improve performance, and reduce storage impacts, when a large burst of events is received, that match a specific criteria.
36. Ako hoces da pretrazis neki event koji sadrzi rec 'virus', sta da radis (u quick search napises virus i to je to)
