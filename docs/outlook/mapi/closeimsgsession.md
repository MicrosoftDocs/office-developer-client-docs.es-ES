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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412040"
---
# <a name="closeimsgsession"></a><span data-ttu-id="31060-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="31060-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="31060-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31060-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31060-105">Cierra una sesión de mensaje y todos los mensajes creados en esa sesión.</span><span class="sxs-lookup"><span data-stu-id="31060-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31060-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="31060-106">Header file:</span></span>  <br/> |<span data-ttu-id="31060-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="31060-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="31060-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="31060-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31060-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31060-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31060-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="31060-110">Called by:</span></span>  <br/> |<span data-ttu-id="31060-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="31060-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="31060-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31060-112">Parameters</span></span>

 <span data-ttu-id="31060-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="31060-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="31060-114">[entrada] Puntero al objeto de sesión de mensaje obtenido mediante la [función OpenIMsgSession](openimsgsession.md) al inicio de la sesión del mensaje.</span><span class="sxs-lookup"><span data-stu-id="31060-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="31060-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31060-115">Return value</span></span>

<span data-ttu-id="31060-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31060-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31060-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31060-117">Remarks</span></span>

<span data-ttu-id="31060-118">Las aplicaciones cliente y los proveedores de servicios que desean tratar con varios objetos **MAPI IMessage** relacionados basados en objetos OLE **IStorage** subyacentes usan una sesión de mensaje.</span><span class="sxs-lookup"><span data-stu-id="31060-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="31060-119">El cliente o el proveedor usa las funciones [OpenIMsgSession](openimsgsession.md) y **CloseIMsgSession** para encapsular la creación de estos mensajes dentro de una sesión de mensaje.</span><span class="sxs-lookup"><span data-stu-id="31060-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="31060-120">Una vez abierta la sesión del mensaje, el cliente o el proveedor le pasa un puntero en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **objeto IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="31060-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="31060-121">Una sesión de mensaje realiza un seguimiento de todos los objetos **IMessage**-on- **IStorage** abiertos durante la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="31060-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="31060-122">Cuando un cliente o proveedor llama **a CloseIMsgSession,** cierra todos estos objetos.</span><span class="sxs-lookup"><span data-stu-id="31060-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="31060-123">Llamar **a CloseIMsgSession** es la única forma de cerrar **objetos IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="31060-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

