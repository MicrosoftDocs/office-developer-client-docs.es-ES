---
title: Carpetas de MAPI oculto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 81b53bc138a64da673d6723e60fd90b086174efe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818135"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="2ba25-103">Carpetas de MAPI oculto</span><span class="sxs-lookup"><span data-stu-id="2ba25-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="2ba25-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ba25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ba25-p101">Carpetas ocultas son gen�rica que los clientes se crean en la carpeta ra�z del almac�n de mensajes, en lugar de en la carpeta ra�z de un sub�rbol de mensajes interpersonales (IPM). Dado que estas carpetas no se colocan en un sub�rbol IPM, por lo general est�n ocultas desde la vista del usuario por el proveedor de almac�n de mensajes. Carpetas ocultas normalmente contienen informaci�n que es relevante para el usuario pero relevantes para el almac�n de mensajes. Los clientes crear las carpetas ocultas para almacenar, por ejemplo, informaci�n adicional que se guarde con el resto de la jerarqu�a de carpetas.</span><span class="sxs-lookup"><span data-stu-id="2ba25-p101">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree. Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider. Hidden folders typically contain information that is relevant to the message store but irrelevant to the user. Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="2ba25-p102">MAPI espera que todos los clientes puedan mostrar, crear, modificar y eliminar carpetas en un sub�rbol IPM. Compatibilidad para trabajar con carpetas en otros �rboles se considera opcional. Sin embargo, todos los almacenes de mensaje que puede usarse como el almac�n predeterminado y que puede enviar y recibir mensajes deben completamente compatible con las carpetas ocultas.</span><span class="sxs-lookup"><span data-stu-id="2ba25-p102">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree. Support for working with folders in other trees is considered optional. However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ba25-112">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="2ba25-112">See also</span></span>



[<span data-ttu-id="2ba25-113">Carpetas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2ba25-113">MAPI Folders</span></span>](mapi-folders.md)
