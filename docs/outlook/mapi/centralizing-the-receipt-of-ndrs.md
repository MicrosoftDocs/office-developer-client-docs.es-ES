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
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579441"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="4472e-103">Centralizar la recepción de NDR</span><span class="sxs-lookup"><span data-stu-id="4472e-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="4472e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4472e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4472e-105">**Para que los informes de no entrega (NDR) entran en una ubicación central cuando se ejecutan simultáneamente varias instancias del cliente**</span><span class="sxs-lookup"><span data-stu-id="4472e-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="4472e-106">Establezca **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) en los valores apropiados para la cuenta que va a recibir los informes.</span><span class="sxs-lookup"><span data-stu-id="4472e-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="4472e-107">Crear el identificador de entrada mediante una llamada a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si es necesario.</span><span class="sxs-lookup"><span data-stu-id="4472e-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="4472e-108">Saber que existen sistemas de mensajería que se va a omitir la cuenta que ha solicitado para los informes y enviarlos al autor de la.</span><span class="sxs-lookup"><span data-stu-id="4472e-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="4472e-109">Reducir el impacto que esto tendrá en los administradores que necesitan para mover informes de alrededor de:</span><span class="sxs-lookup"><span data-stu-id="4472e-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="4472e-110">Mayor que el mensaje original para una clase de mensaje distintos, como IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="4472e-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="4472e-111">Busque los mensajes entrantes con la clase Report.IPM.Note.MSNNews.NDR y reenviarlas a la cuenta pensado para llegar a los informes.</span><span class="sxs-lookup"><span data-stu-id="4472e-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="4472e-112">Al mismo tiempo, enviar correo electrónico al sistema de mensajería que no tiene en cuenta su cuenta de informe de no entrega para comunicar que debe respetar la propiedad **PR_REPORT_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="4472e-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="4472e-113">Sistemas de mensajería más que no se respetan **PR_REPORT_ENTRYID** no respeta las convenciones de clase de mensaje MAPI ya sea.</span><span class="sxs-lookup"><span data-stu-id="4472e-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="4472e-114">Por lo tanto, recibirá algo parecido a una nota.</span><span class="sxs-lookup"><span data-stu-id="4472e-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="4472e-115">Esto es un poco más difícil abordar los problemas con debido a que la entrada es por lo que la variable.</span><span class="sxs-lookup"><span data-stu-id="4472e-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="4472e-116">Examine el asunto y reenviarlo si encuentra puede ser algo de una lista de palabras que Media "sin entregar" o algo desde el asunto de la original.</span><span class="sxs-lookup"><span data-stu-id="4472e-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="4472e-117">Esté preparado para ajustar estas listas a través del tiempo.</span><span class="sxs-lookup"><span data-stu-id="4472e-117">Be prepared to tune these lists over time.</span></span> 
    

