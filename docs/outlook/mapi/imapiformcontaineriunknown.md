---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407532"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="a9471-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9471-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="a9471-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9471-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9471-105">Administra formularios en bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="a9471-105">Manages forms in form libraries.</span></span> <span data-ttu-id="a9471-106">Esta interfaz se usa para crear bibliotecas de formulario específicas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9471-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9471-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a9471-107">Header file:</span></span>  <br/> |<span data-ttu-id="a9471-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a9471-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a9471-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="a9471-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a9471-110">Objetos de contenedor de formularios</span><span class="sxs-lookup"><span data-stu-id="a9471-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="a9471-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a9471-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a9471-112">Proveedores de bibliotecas de formularios</span><span class="sxs-lookup"><span data-stu-id="a9471-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="a9471-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a9471-113">Called by:</span></span>  <br/> |<span data-ttu-id="a9471-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="a9471-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a9471-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a9471-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a9471-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="a9471-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="a9471-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="a9471-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a9471-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="a9471-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a9471-119">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="a9471-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a9471-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="a9471-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="a9471-121">Instala un formulario en un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="a9471-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="a9471-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="a9471-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="a9471-123">Quita un formulario determinado de un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="a9471-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="a9471-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a9471-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="a9471-125">Resuelve una clase de mensaje en su formulario en un contenedor de formularios y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="a9471-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="a9471-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a9471-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="a9471-127">Resuelve un grupo de clases de mensajes en sus formularios en un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.</span><span class="sxs-lookup"><span data-stu-id="a9471-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="a9471-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a9471-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="a9471-129">Devuelve una matriz de las propiedades usadas por todos los formularios instalados en un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="a9471-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="a9471-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="a9471-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="a9471-131">Devuelve el nombre para mostrar de un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="a9471-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="a9471-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a9471-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="a9471-133">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se ha producido en el objeto contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="a9471-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9471-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a9471-134">See also</span></span>



[<span data-ttu-id="a9471-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a9471-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

