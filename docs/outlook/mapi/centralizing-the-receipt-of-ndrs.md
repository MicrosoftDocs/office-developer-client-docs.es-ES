---
title: Centralizar la recepción de NDR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405859"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="484ef-103">Centralizar la recepción de NDR</span><span class="sxs-lookup"><span data-stu-id="484ef-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="484ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="484ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="484ef-105">**Para que los informes nondelivery (NDRs) lleguen a una ubicación central cuando varias instancias del cliente se ejecutan simultáneamente**</span><span class="sxs-lookup"><span data-stu-id="484ef-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="484ef-106">Establezca **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y PR_REPORT_SEARCH_KEY ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) **en** los valores adecuados para la cuenta que va a recibir los informes.</span><span class="sxs-lookup"><span data-stu-id="484ef-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="484ef-107">Cree el identificador de entrada llamando a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si es necesario.</span><span class="sxs-lookup"><span data-stu-id="484ef-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="484ef-108">Comprenda que hay sistemas de mensajería que ignorarán la cuenta que ha solicitado para los informes y las enviarán al autor de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="484ef-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="484ef-109">Reduzca el impacto que esto tendrá en los administradores que tendrán que mover los informes:</span><span class="sxs-lookup"><span data-stu-id="484ef-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="484ef-110">Dar al mensaje original una clase de mensaje distinta, como IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="484ef-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="484ef-111">Busque mensajes entrantes con la clase Report.IPM.Note.MSNNews.NDR y reenvía a la cuenta a la que desea que se presenten los informes.</span><span class="sxs-lookup"><span data-stu-id="484ef-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="484ef-112">Al mismo tiempo, envíe un correo electrónico al sistema de mensajería que omitió su cuenta de informe de no entrega para comunicar que debe respetar la **propiedad PR_REPORT_ENTRYID** cliente.</span><span class="sxs-lookup"><span data-stu-id="484ef-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="484ef-113">La mayoría de los sistemas de mensajería **que PR_REPORT_ENTRYID** no respetarán las convenciones de clase de mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="484ef-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="484ef-114">Por lo tanto, recibirá algo parecido a una nota.</span><span class="sxs-lookup"><span data-stu-id="484ef-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="484ef-115">Esto es un poco más difícil de tratar porque la entrada es tan variable.</span><span class="sxs-lookup"><span data-stu-id="484ef-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="484ef-116">Mira el asunto y reenvía si encuentras algo de una lista de palabras que significan "no se puede entregar" o algo del tema original.</span><span class="sxs-lookup"><span data-stu-id="484ef-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="484ef-117">Esté preparado para ajustar estas listas con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="484ef-117">Be prepared to tune these lists over time.</span></span> 
    

