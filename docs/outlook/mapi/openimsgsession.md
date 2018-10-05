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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389627"
---
# <a name="openimsgsession"></a><span data-ttu-id="bccab-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="bccab-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="bccab-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bccab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bccab-105">Crea y se abre una sesión de mensajería que agrupa los mensajes creados dentro de él.</span><span class="sxs-lookup"><span data-stu-id="bccab-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bccab-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bccab-106">Header file:</span></span>  <br/> |<span data-ttu-id="bccab-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="bccab-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="bccab-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bccab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bccab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bccab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bccab-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bccab-110">Called by:</span></span>  <br/> |<span data-ttu-id="bccab-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bccab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="bccab-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bccab-112">Parameters</span></span>

 <span data-ttu-id="bccab-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="bccab-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="bccab-114">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="bccab-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="bccab-115">Debe usar este método de asignación al trabajar con la interfaz OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) MAPI.</span><span class="sxs-lookup"><span data-stu-id="bccab-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="bccab-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bccab-116">_ulFlags_</span></span>
  
> <span data-ttu-id="bccab-117">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bccab-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="bccab-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="bccab-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="bccab-119">[out] Puntero a un puntero al objeto de sesión del mensaje devuelto.</span><span class="sxs-lookup"><span data-stu-id="bccab-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bccab-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bccab-120">Return value</span></span>

<span data-ttu-id="bccab-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="bccab-121">S_OK</span></span>
  
> <span data-ttu-id="bccab-122">Se abrió la sesión.</span><span class="sxs-lookup"><span data-stu-id="bccab-122">The session was opened.</span></span>
    
<span data-ttu-id="bccab-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bccab-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="bccab-124">_lpMalloc_ o _lppMsgSess_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="bccab-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="bccab-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="bccab-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="bccab-126">Se pasaron indicadores no válidos.</span><span class="sxs-lookup"><span data-stu-id="bccab-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="bccab-127">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bccab-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="bccab-128">Cuando se llama a esta función, un proveedor de servicio o cliente establece el indicador MAPI_UNICODE para crear archivos .msg de Unicode.</span><span class="sxs-lookup"><span data-stu-id="bccab-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="bccab-129">El archivo [Imessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su PR_STORE_SUPPORT_MASK y es compatible con propiedades de Unicode.</span><span class="sxs-lookup"><span data-stu-id="bccab-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bccab-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bccab-130">Remarks</span></span>

<span data-ttu-id="bccab-131">Una sesión de mensajería se usa por las aplicaciones cliente y proveedores de servicios que desean para abordar los problemas con varios relacionados con MAPI [IMessage: IMAPIProp](imessageimapiprop.md) objetos fundamentan objetos OLE **IStorage** subyacentes.</span><span class="sxs-lookup"><span data-stu-id="bccab-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="bccab-132">El cliente o el proveedor utiliza las funciones **OpenIMsgSession** y [CloseIMsgSession](closeimsgsession.md) para ajustar la creación de este tipo de mensajes dentro de una sesión de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bccab-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="bccab-133">Una vez que se abre la sesión de mensajería, el cliente o el proveedor pasa un puntero a ella en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **IMessage**- en - objeto **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="bccab-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="bccab-134">Una sesión de mensajería realiza un seguimiento de todos los **IMessage**- en - objetos **IStorage** creados durante la duración de la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccab-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="bccab-135">Cuando un cliente o un proveedor de llamadas **CloseIMsgSession**, cierra todos estos objetos.</span><span class="sxs-lookup"><span data-stu-id="bccab-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="bccab-136">Al llamar a **CloseIMsgSession** es la única forma de cerrar **IMessage**- en - objetos **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="bccab-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="bccab-137">**OpenIMsgSession** se usa en los clientes y proveedores que requieren la capacidad para manejar varios mensajes relacionados como objetos OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="bccab-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="bccab-138">Si sólo hay un mensaje de este tipo esté abierto en un momento, no es necesario realizar un seguimiento de varios mensajes y no hay motivo para crear una sesión de mensajería con **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="bccab-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="bccab-139">Debido a que se trata de un objeto OLE subyacente, MAPI debe usar la asignación de memoria OLE.</span><span class="sxs-lookup"><span data-stu-id="bccab-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="bccab-140">Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y asignación de memoria OLE, vea [OLE y la transferencia de datos](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="bccab-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

