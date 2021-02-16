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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342122"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="731a1-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="731a1-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="731a1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="731a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="731a1-105">Admite el uso de formularios en tiempo de ejecución configurables en entornos informáticos distribuidos.</span><span class="sxs-lookup"><span data-stu-id="731a1-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="731a1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="731a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="731a1-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="731a1-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="731a1-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="731a1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="731a1-109">Objetos de fábrica de formularios</span><span class="sxs-lookup"><span data-stu-id="731a1-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="731a1-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="731a1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="731a1-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="731a1-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="731a1-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="731a1-112">Called by:</span></span>  <br/> |<span data-ttu-id="731a1-113">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="731a1-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="731a1-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="731a1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="731a1-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="731a1-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="731a1-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="731a1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="731a1-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="731a1-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="731a1-118">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="731a1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="731a1-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="731a1-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="731a1-120">Devuelve un objeto de fábrica de clase para el formulario.</span><span class="sxs-lookup"><span data-stu-id="731a1-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="731a1-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="731a1-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="731a1-122">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de fábrica de formularios.</span><span class="sxs-lookup"><span data-stu-id="731a1-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="731a1-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="731a1-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="731a1-124">Mantiene un servidor de formulario abierto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="731a1-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="731a1-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="731a1-125">Remarks</span></span>

<span data-ttu-id="731a1-126">La **interfaz IMAPIFormFactory** se basa en la interfaz [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) y los objetos que implementan **IMAPIFormFactory** también deben heredar de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="731a1-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="731a1-127">**IMAPIFormFactory** es la interfaz que los visores de formularios usan para crear nuevos objetos de formulario cuando un servidor de formulario admite más de una clase de mensaje (es decir, más de un tipo de objeto de formulario).</span><span class="sxs-lookup"><span data-stu-id="731a1-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="731a1-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="731a1-128">See also</span></span>



[<span data-ttu-id="731a1-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="731a1-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

