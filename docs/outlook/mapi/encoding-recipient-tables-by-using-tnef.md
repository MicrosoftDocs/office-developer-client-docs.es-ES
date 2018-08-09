---
title: Codificar tablas de destinatario con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816768"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="c8887-103">Codificar tablas de destinatario con TNEF</span><span class="sxs-lookup"><span data-stu-id="c8887-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="c8887-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8887-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8887-105">La codificación de una tabla de destinatario en la secuencia TNEF es rara vez es necesaria dado que los sistemas de mensajería más admiten las listas de destinatarios directamente.</span><span class="sxs-lookup"><span data-stu-id="c8887-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="c8887-106">En general, las propiedades del destinatario se transmiten en el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c8887-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="c8887-107">Cuando es necesaria la inclusión de la tabla de destinatarios, TNEF puede codificar la tabla de destinatarios como parte de su procesamiento habitual.</span><span class="sxs-lookup"><span data-stu-id="c8887-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="c8887-108">Esto se realiza durante la fase inicial de procesamiento de TNEF.</span><span class="sxs-lookup"><span data-stu-id="c8887-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="c8887-109">El proveedor de transporte puede incluir la tabla de destinatarios del mensaje llamando al método [ITnef::AddProps](itnef-addprops.md) con la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada en la lista de inclusión.</span><span class="sxs-lookup"><span data-stu-id="c8887-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="c8887-110">TNEF Obtiene la tabla de destinatarios del mensaje, consulta el conjunto de columnas y procesa cada fila de la tabla en la secuencia de TNEF.</span><span class="sxs-lookup"><span data-stu-id="c8887-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="c8887-111">Un método alternativo está disponible si el proveedor de transporte que se necesita modificar la tabla de destinatarios antes de que se codifica.</span><span class="sxs-lookup"><span data-stu-id="c8887-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="c8887-112">El proveedor de transporte puede construir la tabla es necesaria y, a continuación, llame al método [ITnef::EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="c8887-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="c8887-113">Si se pasa NULL en el parámetro _lpRecipTable_ , tal como se describe para **ITnef::AddProps**, a continuación, la tabla de destinatarios se toma directamente desde el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c8887-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

