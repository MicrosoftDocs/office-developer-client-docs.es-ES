---
title: Codificación de tablas de destinatarios mediante TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417962"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="74174-103">Codificación de tablas de destinatarios mediante TNEF</span><span class="sxs-lookup"><span data-stu-id="74174-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="74174-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74174-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74174-105">La codificación de una tabla de destinatarios en la secuencia TNEF rara vez es necesaria, ya que la mayoría de los sistemas de mensajería admiten listas de destinatarios directamente.</span><span class="sxs-lookup"><span data-stu-id="74174-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="74174-106">En general, las propiedades del destinatario se transmiten en el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="74174-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="74174-107">Cuando es necesaria la inclusión de la tabla de destinatarios, TNEF puede codificar la tabla de destinatarios como parte de su procesamiento habitual.</span><span class="sxs-lookup"><span data-stu-id="74174-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="74174-108">Esto se realiza durante la fase inicial del procesamiento de TNEF.</span><span class="sxs-lookup"><span data-stu-id="74174-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="74174-109">El proveedor de transporte puede incluir la tabla de destinatarios del mensaje llamando al método [ITnef::AddProps](itnef-addprops.md) con la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada en la lista de inclusión.</span><span class="sxs-lookup"><span data-stu-id="74174-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="74174-110">TNEF obtiene la tabla de destinatarios del mensaje, consulta el conjunto de columnas y procesa todas las filas de la tabla en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="74174-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="74174-111">Hay un método alternativo disponible si el proveedor de transporte necesita modificar la tabla de destinatarios antes de codificarse.</span><span class="sxs-lookup"><span data-stu-id="74174-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="74174-112">El proveedor de transporte puede construir la tabla necesaria y, a continuación, llamar al [método ITnef::EncodeRecips.](itnef-encoderecips.md)</span><span class="sxs-lookup"><span data-stu-id="74174-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="74174-113">Si se pasa NULL en el parámetro  _lpRecipTable,_ la tabla de destinatarios se toma directamente del mensaje tal como se describe para **ITnef::AddProps**.</span><span class="sxs-lookup"><span data-stu-id="74174-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

