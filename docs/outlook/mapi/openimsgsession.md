---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326197"
---
# <a name="openimsgsession"></a><span data-ttu-id="624b4-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="624b4-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="624b4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="624b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="624b4-105">Crea y abre una sesión de mensaje que agrupa los mensajes creados en ella.</span><span class="sxs-lookup"><span data-stu-id="624b4-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="624b4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="624b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="624b4-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="624b4-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="624b4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="624b4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="624b4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="624b4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="624b4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="624b4-110">Called by:</span></span>  <br/> |<span data-ttu-id="624b4-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="624b4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="624b4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="624b4-112">Parameters</span></span>

 <span data-ttu-id="624b4-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="624b4-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="624b4-114">[in] Puntero a un objeto de asignador de memoria que expone la [interfaz OLE IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)</span><span class="sxs-lookup"><span data-stu-id="624b4-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="624b4-115">MAPI debe usar este método de asignación al trabajar con la interfaz OLE [IStorage.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)</span><span class="sxs-lookup"><span data-stu-id="624b4-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="624b4-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="624b4-116">_ulFlags_</span></span>
  
> <span data-ttu-id="624b4-117">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="624b4-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="624b4-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="624b4-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="624b4-119">[salida] Puntero a un puntero al objeto de sesión de mensaje devuelto.</span><span class="sxs-lookup"><span data-stu-id="624b4-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="624b4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="624b4-120">Return value</span></span>

<span data-ttu-id="624b4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="624b4-121">S_OK</span></span>
  
> <span data-ttu-id="624b4-122">Se abrió la sesión.</span><span class="sxs-lookup"><span data-stu-id="624b4-122">The session was opened.</span></span>
    
<span data-ttu-id="624b4-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="624b4-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="624b4-124">_lpMalloc_ o  _lppMsgSess_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="624b4-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="624b4-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="624b4-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="624b4-126">Se pasaron marcas no válidas.</span><span class="sxs-lookup"><span data-stu-id="624b4-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="624b4-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="624b4-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="624b4-128">Al llamar a esta función, un cliente o proveedor de servicios establece la marca MAPI_UNICODE para crear archivos .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="624b4-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="624b4-129">El archivo [Imessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su PR_STORE_SUPPORT_MASK y admite propiedades Unicode.</span><span class="sxs-lookup"><span data-stu-id="624b4-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="624b4-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="624b4-130">Remarks</span></span>

<span data-ttu-id="624b4-131">Las aplicaciones cliente y los proveedores de servicios usan una sesión de mensajes que desean tratar varios objetos IMessage de MAPI [relacionados: IMAPIProp](imessageimapiprop.md) creados sobre objetos OLE **IStorage** subyacentes.</span><span class="sxs-lookup"><span data-stu-id="624b4-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="624b4-132">El cliente o el proveedor usa las **funciones OpenIMsgSession** y [CloseIMsgSession](closeimsgsession.md) para encapsular la creación de dichos mensajes dentro de una sesión de mensaje.</span><span class="sxs-lookup"><span data-stu-id="624b4-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="624b4-133">Una vez abierta la sesión del mensaje, el cliente o el proveedor le pasa un puntero en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **objeto IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="624b4-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="624b4-134">Una sesión de mensaje realiza un seguimiento de todos los objetos **IMessage**-on- **IStorage** creados durante la duración de la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="624b4-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="624b4-135">Cuando un cliente o proveedor llama **a CloseIMsgSession**, cierra todos estos objetos.</span><span class="sxs-lookup"><span data-stu-id="624b4-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="624b4-136">Llamar **a CloseIMsgSession** es la única forma de cerrar **objetos IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="624b4-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="624b4-137">Los clientes y proveedores usan **OpenIMsgSession** para controlar varios mensajes relacionados como objetos OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="624b4-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="624b4-138">Si solo se va a abrir uno de estos mensajes a la vez, no es necesario realizar un seguimiento de varios mensajes ni motivo para crear una sesión de mensaje con **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="624b4-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="624b4-139">Dado que se trata de un objeto OLE subyacente, MAPI debe usar la asignación de memoria OLE.</span><span class="sxs-lookup"><span data-stu-id="624b4-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="624b4-140">Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y la asignación de memoria OLE, vea [OLE y Transferencia de datos](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="624b4-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

