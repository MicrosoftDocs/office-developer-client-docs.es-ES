---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384769"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="cfa94-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfa94-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="cfa94-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfa94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfa94-105">Admite el uso de formularios configurables de tiempo de ejecución en entornos de sistemas distribuidos.</span><span class="sxs-lookup"><span data-stu-id="cfa94-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cfa94-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cfa94-106">Header file:</span></span>  <br/> |<span data-ttu-id="cfa94-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="cfa94-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="cfa94-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="cfa94-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="cfa94-109">Objetos de generador de formulario</span><span class="sxs-lookup"><span data-stu-id="cfa94-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="cfa94-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="cfa94-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cfa94-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="cfa94-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="cfa94-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="cfa94-112">Called by:</span></span>  <br/> |<span data-ttu-id="cfa94-113">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="cfa94-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="cfa94-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="cfa94-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cfa94-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="cfa94-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="cfa94-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="cfa94-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="cfa94-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="cfa94-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cfa94-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="cfa94-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cfa94-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="cfa94-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="cfa94-120">Devuelve un objeto de fábrica de clase para el formulario.</span><span class="sxs-lookup"><span data-stu-id="cfa94-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="cfa94-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="cfa94-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="cfa94-122">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen al objeto de fábrica de formulario.</span><span class="sxs-lookup"><span data-stu-id="cfa94-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="cfa94-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="cfa94-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="cfa94-124">Mantiene un servidor de formulario abierto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="cfa94-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfa94-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfa94-125">Remarks</span></span>

<span data-ttu-id="cfa94-126">La interfaz de **IMAPIFormFactory** se basa en la interfaz [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) y los objetos que implementan **IMAPIFormFactory** también deben heredar de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="cfa94-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="cfa94-127">**IMAPIFormFactory** es la interfaz que los visores de formulario que se usa para crear nuevos objetos de formulario cuando un servidor de formulario es compatible con más de una clase de mensaje (es decir, más de un tipo de objeto de formulario).</span><span class="sxs-lookup"><span data-stu-id="cfa94-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cfa94-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfa94-128">See also</span></span>



[<span data-ttu-id="cfa94-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="cfa94-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

