---
title: IUnknown IMAPIFormFactory
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342122"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="6be60-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6be60-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="6be60-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6be60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6be60-105">Admite el uso de formularios configurables en tiempo de ejecución en entornos informáticos distribuidos.</span><span class="sxs-lookup"><span data-stu-id="6be60-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6be60-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6be60-106">Header file:</span></span>  <br/> |<span data-ttu-id="6be60-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="6be60-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6be60-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="6be60-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6be60-109">Objetos de la factoría de formularios</span><span class="sxs-lookup"><span data-stu-id="6be60-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="6be60-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6be60-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6be60-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="6be60-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="6be60-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6be60-112">Called by:</span></span>  <br/> |<span data-ttu-id="6be60-113">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="6be60-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="6be60-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="6be60-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6be60-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="6be60-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="6be60-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="6be60-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6be60-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="6be60-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6be60-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="6be60-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6be60-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="6be60-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="6be60-120">Devuelve un objeto de generador de clases para el formulario.</span><span class="sxs-lookup"><span data-stu-id="6be60-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="6be60-121">Volvió</span><span class="sxs-lookup"><span data-stu-id="6be60-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="6be60-122">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de generador de formularios.</span><span class="sxs-lookup"><span data-stu-id="6be60-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="6be60-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="6be60-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="6be60-124">Mantiene un servidor de formulario abierto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="6be60-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6be60-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6be60-125">Remarks</span></span>

<span data-ttu-id="6be60-126">La interfaz **IMAPIFormFactory** se basa en la interfaz [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) y los objetos que implementan **IMAPIFormFactory** también deben heredar de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="6be60-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="6be60-127">**IMAPIFormFactory** es la interfaz que los visores de formularios usan para crear nuevos objetos de formulario cuando un servidor de formularios admite más de una clase de mensaje (es decir, más de un tipo de objeto de formulario).</span><span class="sxs-lookup"><span data-stu-id="6be60-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6be60-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6be60-128">See also</span></span>



[<span data-ttu-id="6be60-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6be60-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

