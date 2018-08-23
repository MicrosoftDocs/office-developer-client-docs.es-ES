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
ms.openlocfilehash: f358467d72f2a9f395762f529244041a5d9d8d6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575983"
---
# <a name="closeimsgsession"></a><span data-ttu-id="55d03-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="55d03-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="55d03-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55d03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55d03-105">Cierra una sesión de mensajería y todos los mensajes creados dentro de esa sesión.</span><span class="sxs-lookup"><span data-stu-id="55d03-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55d03-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="55d03-106">Header file:</span></span>  <br/> |<span data-ttu-id="55d03-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="55d03-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="55d03-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="55d03-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="55d03-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="55d03-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="55d03-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="55d03-110">Called by:</span></span>  <br/> |<span data-ttu-id="55d03-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="55d03-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="55d03-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55d03-112">Parameters</span></span>

 <span data-ttu-id="55d03-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="55d03-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="55d03-114">[entrada] Puntero para el objeto de sesión de mensaje obtenido mediante la función [OpenIMsgSession](openimsgsession.md) al principio de la sesión de mensajería.</span><span class="sxs-lookup"><span data-stu-id="55d03-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="55d03-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55d03-115">Return value</span></span>

<span data-ttu-id="55d03-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55d03-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55d03-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55d03-117">Remarks</span></span>

<span data-ttu-id="55d03-118">Una sesión de mensajería se usa en las aplicaciones cliente y proveedores de servicios que desean para abordar los problemas con varios objetos MAPI **IMessage** relacionados fundamentan objetos OLE **IStorage** subyacentes.</span><span class="sxs-lookup"><span data-stu-id="55d03-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="55d03-119">El cliente o el proveedor utiliza las funciones [OpenIMsgSession](openimsgsession.md) y **CloseIMsgSession** para ajustar la creación de este tipo de mensajes dentro de una sesión de mensajería.</span><span class="sxs-lookup"><span data-stu-id="55d03-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="55d03-120">Una vez que se abre la sesión de mensajería, el cliente o el proveedor pasa un puntero a ella en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **IMessage**- en - objeto **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="55d03-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="55d03-121">Una sesión de mensajería realiza un seguimiento de todos los objetos de **IMessage**- en - **IStorage** abiertos durante la duración de la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="55d03-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="55d03-122">Cuando un cliente o un proveedor de llamadas **CloseIMsgSession**, cierra todos estos objetos.</span><span class="sxs-lookup"><span data-stu-id="55d03-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="55d03-123">Al llamar a **CloseIMsgSession** es la única forma de cerrar **IMessage**- en - objetos **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="55d03-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

