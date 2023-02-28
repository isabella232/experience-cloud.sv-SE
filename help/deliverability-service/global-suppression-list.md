---
title: Global undertryckningslista
description: Upptäck den globala listan över inaktiveringar
hide: true
source-git-commit: a946cfb1027896f6e45aaf88d25ad7114d6b5ac6
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Global undertryckningslista {#global-suppression-list}

En inaktiveringslista består av e-postadresser som kunderna vill utesluta från leveranser, eftersom det kan skada deras sändningsrykte och leveransfrekvenser om de skickar till dessa kontakter. För närvarande håller Adobe en uppdaterad lista över kända dåliga e-postadresser som har visat sig vara skadliga för engagemanget och utskickets anseende och ser till att e-post inte skickas till dem. Den här listan hanteras i en global undertryckningslista som är gemensam för alla Adobe-kunder. Adresserna och domännamnen som finns i den globala undertryckningslistan är dolda. Endast antalet uteslutna mottagare anges i leveransrapporterna.

Nu går det att hantera den globala undertryckningslistan från ett gränssnitt som är tillgängligt internt. Denna lista kommer endast att underhållas av leveranskonsulter. Den globala undertryckningslistan kan innehålla e-post- eller domänadresser.

## Åtkomst till den globala listan över inaktiveringar

Om du vill få tillgång till den detaljerade listan över e-postadresser och domäner som inte ingår går du till **[!UICONTROL Gloabl suppression list]**.

>[!CAUTION]
>
>Behörigheter att visa, exportera och hantera den globala undertryckningslistan beror på den distributionslista som du har tilldelats. Läs mer

Två flikar visas: **[!UICONTROL Email]** och **[!UICONTROL Domain]**.

Det finns filter som hjälper dig att bläddra igenom listan.

## Lägga till adresser och domäner

Det finns för närvarande två sätt som adresser läggs till i den globala listan över undertryckningar:

* Lista strukturerad av leveransgruppen.
* Lista från tredjeparts tjänsteleverantör Blackbox.

Du kan lägga till e-postadresser eller domäner [en åt gången](#add-one-address-or-domain), eller [i gruppläge](#upload-csv-file) via en CSV-filöverföring.

Om du vill göra det väljer du **[!UICONTROL Add email or domain]** och därefter någon av metoderna nedan.

### Lägg till en adress eller domän {#add-one-address-or-domain}

1. Välj **[!UICONTROL One by one]** alternativ.

1. Välj adresstyp: **[!UICONTROL Email address]** eller **[!UICONTROL Domain address]**.

1. Ange den e-postadress eller domän som du vill utesluta från sändningen.

   >[!NOTE]
   >
   >Kontrollera att du anger en giltig e-postadress (till exempel abc@company.com) eller domän (till exempel abc.company.com).

1. Ange en orsak om det behövs.

   >[!NOTE]
   >
   >Alla ASCII-utskrivbara tecken mellan 32 och 126 är tillåtna i det här fältet. Den fullständiga listan finns på [den här sidan](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"} till exempel.

1. Klicka på **[!UICONTROL Submit]** för att bekräfta.

### Överföra en CSV-fil {#upload-csv-file}

1. Välj **[!UICONTROL Upload CSV]** alternativ.

1. Ladda ned CSV-mallen som ska användas, som innehåller kolumnerna och formatet nedan:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```
   >[!CAUTION]
   >
   >Ändra inte namnen på kolumnerna i CSV-mallen.
   >
   >Filstorleken får inte överstiga 1 MB.

1. Fyll i CSV-mallen med de e-postadresser och/eller domäner som du vill lägga till i listan över inaktiveringar.

   >[!NOTE]
   >
   >Alla ASCII-tecken mellan 32 och 126 tillåts i **Kommentar** kolumn. Den fullständiga listan finns på [den här sidan](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"} till exempel.

1. När du är klar drar och släpper du CSV-filen och klickar sedan på **[!UICONTROL Submit]** för att bekräfta.

>[!NOTE]
>
>När överföringen är klar kontrollerar du att den lyckades genom att kontrollera dess status från gränssnittet. [Lär dig mer](#recent-uploads)

### Kontrollera status för senaste överföringar {#recent-uploads}

Klicka på **[!UICONTROL Recent uploads]** för att kontrollera status för de senaste CSV-filerna du överfört.

Möjliga statusar är:

* **[!UICONTROL Pending]**: Filöverföringen bearbetas.
* **[!UICONTROL Error]**: Filöverföringen misslyckades på grund av ett tekniskt fel eller ett filformatsfel.
* **[!UICONTROL Complete]**: Filöverföringen har slutförts.

Om vissa adresser inte har rätt format läggs de inte till i den globala listan över undertryckningar under överföringen.

När överföringen är klar kopplas den då till en rapport. Du kan hämta den för att kontrollera de fel som påträffats.

## Ta bort adresser

Om du vill ta bort en adress från den globala listan över inaktiveringar använder du **[!UICONTROL Delete]** -knappen.

>[!CAUTION]
>
>Adresser eller domäner som läggs till automatiskt av tredjeparts tjänsteleverantör Blackbox kan inte tas bort av konsulter via gränssnittet. Detta kan endast göras via en backend-biljett.
