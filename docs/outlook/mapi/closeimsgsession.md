---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334940"
---
# <a name="closeimsgsession"></a><span data-ttu-id="750e7-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="750e7-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="750e7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="750e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="750e7-105">Cierra una sesión de mensajes y todos los mensajes creados en esa sesión.</span><span class="sxs-lookup"><span data-stu-id="750e7-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="750e7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="750e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="750e7-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="750e7-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="750e7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="750e7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="750e7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="750e7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="750e7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="750e7-110">Called by:</span></span>  <br/> |<span data-ttu-id="750e7-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="750e7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="750e7-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="750e7-112">Parameters</span></span>

 <span data-ttu-id="750e7-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="750e7-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="750e7-114">a Puntero al objeto de sesión de mensaje obtenido mediante la función [OpenIMsgSession](openimsgsession.md) al inicio de la sesión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="750e7-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="750e7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="750e7-115">Return value</span></span>

<span data-ttu-id="750e7-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="750e7-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="750e7-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="750e7-117">Remarks</span></span>

<span data-ttu-id="750e7-118">Las aplicaciones cliente y los proveedores de servicios utilizan una sesión de mensajes que desean tratar con varios objetos MAPI **IMessage** relacionados creados sobre objetos OLE **IStorage** subyacentes.</span><span class="sxs-lookup"><span data-stu-id="750e7-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="750e7-119">El cliente o el proveedor usa las funciones [OpenIMsgSession](openimsgsession.md) y **CloseIMsgSession** para encapsular la creación de dichos mensajes dentro de una sesión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="750e7-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="750e7-120">Una vez abierta la sesión de mensajes, el cliente o el proveedor pasa un puntero a ella en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo objeto **IMessage**-on- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="750e7-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="750e7-121">Una sesión de mensajes realiza un seguimiento de todos los objetos **IMessage**en **IStorage** abiertos durante la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="750e7-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="750e7-122">Cuando un cliente o proveedor llama a **CloseIMsgSession**, cierra todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="750e7-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="750e7-123">Llamar a **CloseIMsgSession** es la única forma de cerrar objetos **IMessage**-on- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="750e7-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

