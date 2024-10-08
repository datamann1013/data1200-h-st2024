:::mermaid

flowchart TD

Start ((Start))

Slutt((Slutt))

SettInn(Sett inn panteobjekt)
TaUt(Ta ut pantebeløp)
LeggTilBelop(Legg til pantebeløp)
skrivUtLogg(Skriv ut lodd)
SkrivUtKvittering(Skriv ut kvittering)

godkjent{Godkjent?}
fortsett{Fortsett?}
ferdig{Godkjent eller lodd?}

Start ---> SettInn
SettInn ---> godkjent

godkjent--JA-->LeggtilBelop 
godkjent --NEI--> TaUt

LeggTilBelop --> fortsett
TaUt --> fortsett

fortsett --JA-->SettInn
fortsett --NEI--> ferdig

ferdig--lodd-->SkrivUtLodd
ferdig--kvittering--> skrivUtKvittering

SkrivUtKvittering --> Slutt
SkrivUtLodd --> Slutt



:::