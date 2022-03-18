API
===

<h1 id="complete-wds-handleiding">Complete WDS handleiding</h1>
<p>In deze handleiding leer je hoe je een complete WDS maakt en hoe je het examen makkelijk klaart.</p>
<h2 id="hoofdstukken">Hoofdstukken</h2>
<ul>
<li><a href="#vmware-netwerk-instellen">VMWare netwerk instellen</a></li>
<li><a href="#windows-server-2022-vm-aanmaken">Windows Server 2022 VM aanmaken</a></li>
<li><a href="#basis-installatie-windows-server-2022-installeren">Basis installatie Windows Server 2022 installeren</a></li>
<li><a href="#tweede-schijf-aanmaken-op-de-server-voor-flexibiliteit">Tweede schijf aanmaken op de server voor flexibiliteit</a></li>
<li><a href="#windows-server-2022-installeren">Windows Server 2022 installeren</a></li>
</ul>
<hr />
<h3 id="vmware-netwerk-instellen">VMWare netwerk instellen</h3>
<p><img src="https://i.ibb.co/zxDqgHp/1.png" alt="" />
Ga hiernaartoe en klik op de knop <strong>Change settings</strong>.</p>
<h2 id="zorg-ervoor-dat-vmnet1-geselecteerd-is-en-dat-use-local-dhcp-service-to-distribute-ip-address-to-vms-uit-is.info-deze-instelling-is-belangrijk-omdat-we-op-de-server-een-eigen-dhcp-server-gaan-gebruiken-en-die-dus-ook-willen-hebben.zonder-deze-instelling-zou-onze-flaptop-het-werkstation-een-ip-adres-geven-en-dan-werkt-het-niet"><img src="https://i.ibb.co/hsDDkLB/2.png" alt="" />
Zorg ervoor dat <strong>VMnet1</strong> geselecteerd is en dat <strong>Use local DHCP service to distribute IP address to VMs</strong> uit is.
<strong>INFO: Deze instelling is belangrijk, omdat we op de server een eigen DHCP server gaan gebruiken en die dus ook willen hebben. Zonder deze instelling zou onze flaptop het werkstation een IP adres geven en dan werkt het niet.</strong></h2>
<h3 id="windows-server-2022-vm-aanmaken">Windows Server 2022 VM aanmaken</h3>
<p><img src="https://i.ibb.co/ZK2Gjzw/1.png" alt="" />
Maak een nieuwe virtuele machine aan en gebruik de typical installation.</p>
<p><img src="https://i.ibb.co/Xy7cQ7j/2.png" alt="" />
Kies de Windows Server 2022 ISO.</p>
<p><img src="https://i.ibb.co/R08FqGb/3.png" alt="" />
Stel de instellingen in zoals op de foto met jouw eigen wachtwoord.
<strong>TIP: Zorg ervoor dat je een goed wachtwoord hebt omdat je dit vaak nodig zal hebben.</strong>
<strong>INFO: Licentie en Windows type boeit niet. VMWare detecteert niet dat we een Windows Server image gebruiken.</strong></p>
<p><img src="https://i.ibb.co/chFn2Gh/4.png" alt="" />
Geef de virtuele machine een naam.
<strong>TIP: Maak het simpel, en niet lang.</strong></p>
<p><img src="https://i.ibb.co/QF5pBWn/5.png" alt="" />
Stel de bovenstaande instellingen in.
<strong>INFO: We kiezen single file zodat de virtuele machine sneller zichzelf kan laden.</strong></p>
<p><img src="https://i.ibb.co/c6D06x6/6.png" alt="" />
Klik op de knop <strong>Customize Hardware</strong>.</p>
<h2 id="stel-bovenstaande-instellingen-in.klik-dan-op-de-knop-finish"><img src="https://i.ibb.co/mCSVx7Q/7.png" alt="" />
Stel bovenstaande instellingen in. Klik dan op de knop <strong>Finish</strong>.</h2>
<h3 id="basis-installatie-windows-server-2022-installeren">Basis installatie Windows Server 2022 installeren</h3>
<p><img src="https://i.ibb.co/z85D8YP/1.png" alt="" />
Start de server op en je krijgt dit scherm.</p>
<p><img src="https://i.ibb.co/t89xKLW/2.png" alt="" />
Kies de 2e optie zodat je een grafische interface hebt. De server gaat nu installeren.</p>
<p><img src="https://i.ibb.co/6mFT5cc/3.png" alt="" />
De server begint nu aan first time startup en zal VMWare tools installeren. Laat dit gebeuren want alles gaat vanzelf en de server zal zichzelf herstarten.
<strong>INFO: Je kan zien dat er rechtsonder een wereldbol staat. Als je dit hebt dan heb je alles goed ingesteld in termen van VMWare netwerken.</strong></p>
<p><img src="https://i.ibb.co/T1zyDnG/4.png" alt="" />
Log nu in met het wachtwoord dat je hebt gemaakt.</p>
<h2 id="haal-deze-kutmelding-weg"><img src="https://i.ibb.co/gdH8Pkh/5.png" alt="" />
Haal deze kutmelding weg.</h2>
<h3 id="tweede-schijf-aanmaken-op-de-server-voor-flexibiliteit">Tweede schijf aanmaken op de server voor flexibiliteit</h3>
<p><img src="https://i.ibb.co/SRhQdmF/1.png" alt="" />
Zoek naar <strong>Disk Management</strong> en open het.</p>
<p><img src="https://i.ibb.co/SBdQBz9/2.png" alt="" />
Klik met de rechtermuisknop op <strong>(C:)</strong> en klik op <strong>Shrink Volume</strong>.</p>
<p><img src="https://i.ibb.co/xjmDvmf/3.png" alt="" />
Stel amount to shrink in naar <strong>50 000</strong> (50gb dus) en klik op <strong>Shrink</strong>.</p>
<p><img src="https://i.ibb.co/nB3MdH9/4.png" alt="" />
Klik met de rechtermuisknop op dit nieuwe stuk en klik op <strong>New Simple Volume</strong></p>
<p><img src="https://i.ibb.co/q9GBVYp/5.png" alt="" />
Next.</p>
<p><img src="https://i.ibb.co/frVjRxy/6.png" alt="" />
We willen alles, next.</p>
<p><img src="https://i.ibb.co/j6Fw4Qd/7.png" alt="" />
Zorg ervoor dat de drive letter op <strong>E</strong> staat omdat ik dit gebruik in de handleiding. Next.</p>
<p><img src="https://i.ibb.co/NyCCfXw/8.png" alt="" />
Stel bovenstaande instellingen. Next.</p>
<p><img src="https://i.ibb.co/1LLx7fj/9.png" alt="" />
Finish.</p>
<p><img src="https://i.ibb.co/5r15MkK/10.png" alt="" />
Maak deze 2 mapjes aan op de nieuwe schijf.</p>
<h2 id="sleep-je-windows-mapje-met-daarin-de-rauwe-windows-bestanden-in-images.dit-krijg-je-van-de-leraar-bij-het-examen"><img src="https://i.ibb.co/YbFZkyR/11.png" alt="" />
Sleep je Windows mapje met daarin de rauwe Windows bestanden in <strong>Images</strong>. Dit krijg je van de leraar bij het examen.</h2>
<h3 id="windows-server-2022-installeren">Windows Server 2022 installeren</h3>
