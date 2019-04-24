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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332665"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="362d6-103">Centralizar la recepción de NDR</span><span class="sxs-lookup"><span data-stu-id="362d6-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="362d6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="362d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="362d6-105">**Para que los informes de no entrega (NDR) lleguen a una ubicación central cuando se ejecuten simultáneamente varias instancias del cliente**</span><span class="sxs-lookup"><span data-stu-id="362d6-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="362d6-106">Establecer **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) en los valores apropiados para la cuenta que va a recibir los informes.</span><span class="sxs-lookup"><span data-stu-id="362d6-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="362d6-107">Cree el identificador de entrada llamando a [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) si es necesario.</span><span class="sxs-lookup"><span data-stu-id="362d6-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="362d6-108">Comprenda que hay sistemas de mensajería que ignorarán la cuenta que ha solicitado para los informes y que los enviarán al autor.</span><span class="sxs-lookup"><span data-stu-id="362d6-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="362d6-109">Reduzca el impacto que esto tendrá en los administradores que tendrán que mover los informes de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="362d6-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="362d6-110">Dar a su mensaje original una clase de mensaje distinta, como IPM. Note. MSNNews.</span><span class="sxs-lookup"><span data-stu-id="362d6-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="362d6-111">Busque los mensajes entrantes con la clase rePort. IPM. Note. MSNNews. NDR y reenvíelos a la cuenta a la que ha pensado para llegar los informes.</span><span class="sxs-lookup"><span data-stu-id="362d6-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="362d6-112">Al mismo tiempo, envíe un correo electrónico al sistema de mensajería que haya ignorado su cuenta de informe de no entrega para comunicar que debe seguir la propiedad **PR_REPORT_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="362d6-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="362d6-113">La mayoría de los sistemas de mensajería que no respetan **PR_REPORT_ENTRYID** no cumplirán las convenciones de clase de mensaje de MAPI tampoco.</span><span class="sxs-lookup"><span data-stu-id="362d6-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="362d6-114">Por lo tanto, recibirá algo parecido a una nota.</span><span class="sxs-lookup"><span data-stu-id="362d6-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="362d6-115">Esto es un poco más difícil de tratar porque la entrada es tan variable.</span><span class="sxs-lookup"><span data-stu-id="362d6-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="362d6-116">Mire el asunto y reenvíelo si encuentra algo de una lista de palabras que significa "no se puede entregar" o algo del asunto original.</span><span class="sxs-lookup"><span data-stu-id="362d6-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="362d6-117">Prepárese para ajustar estas listas con el paso del tiempo.</span><span class="sxs-lookup"><span data-stu-id="362d6-117">Be prepared to tune these lists over time.</span></span> 
    

