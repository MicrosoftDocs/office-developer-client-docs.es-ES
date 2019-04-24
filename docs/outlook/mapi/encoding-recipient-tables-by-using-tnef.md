---
title: Codificar tablas de destinatarios mediante TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339406"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="c9404-103">Codificar tablas de destinatarios mediante TNEF</span><span class="sxs-lookup"><span data-stu-id="c9404-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="c9404-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9404-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9404-105">La codificación de una tabla de destinatarios en la secuencia TNEF rara vez es necesaria, ya que la mayoría de los sistemas de mensajería admiten listas de destinatarios directamente.</span><span class="sxs-lookup"><span data-stu-id="c9404-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="c9404-106">En general, las propiedades del destinatario se transmiten en el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9404-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="c9404-107">Cuando se necesita la inclusión de la tabla de destinatarios, TNEF puede codificar la tabla de destinatarios como parte de su procesamiento habitual.</span><span class="sxs-lookup"><span data-stu-id="c9404-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="c9404-108">Esto se realiza durante la fase inicial del procesamiento TNEF.</span><span class="sxs-lookup"><span data-stu-id="c9404-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="c9404-109">El proveedor de transporte puede incluir la tabla de destinatarios del mensaje llamando al método [ITnef:: AddProps](itnef-addprops.md) con la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada en la lista de inclusión.</span><span class="sxs-lookup"><span data-stu-id="c9404-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="c9404-110">TNEF obtiene la tabla de destinatarios del mensaje, consulta el conjunto de columnas y procesa todas las filas de la tabla en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="c9404-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="c9404-111">Hay disponible un método alternativo si el proveedor de transporte necesita modificar la tabla de destinatarios antes de codificarla.</span><span class="sxs-lookup"><span data-stu-id="c9404-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="c9404-112">El proveedor de transporte puede construir la tabla necesaria y, a continuación, llamar al método [ITnef:: EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="c9404-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="c9404-113">Si se pasa NULL en el parámetro _lpRecipTable_ , la tabla de destinatarios se obtiene directamente del mensaje, tal y como se describe para **ITnef:: AddProps**.</span><span class="sxs-lookup"><span data-stu-id="c9404-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

