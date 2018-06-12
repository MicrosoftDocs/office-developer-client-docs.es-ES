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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817285"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="d26d6-103">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d26d6-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="d26d6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d26d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d26d6-105">Administra formularios en las bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="d26d6-105">Manages forms in form libraries.</span></span> <span data-ttu-id="d26d6-106">Esta interfaz se usa para crear bibliotecas de formularios específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d26d6-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d26d6-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d26d6-107">Header file:</span></span>  <br/> |<span data-ttu-id="d26d6-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="d26d6-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d26d6-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="d26d6-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="d26d6-110">Objetos de contenedor de formulario</span><span class="sxs-lookup"><span data-stu-id="d26d6-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="d26d6-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d26d6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d26d6-112">Proveedores de biblioteca de formulario</span><span class="sxs-lookup"><span data-stu-id="d26d6-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="d26d6-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d26d6-113">Called by:</span></span>  <br/> |<span data-ttu-id="d26d6-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="d26d6-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="d26d6-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="d26d6-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d26d6-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="d26d6-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="d26d6-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="d26d6-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="d26d6-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="d26d6-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d26d6-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="d26d6-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d26d6-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="d26d6-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="d26d6-121">Instala un formulario en un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d26d6-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="d26d6-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="d26d6-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="d26d6-123">Quita un formulario en particular de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d26d6-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="d26d6-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="d26d6-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="d26d6-125">Una clase de mensaje se resuelve en su formulario en un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="d26d6-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="d26d6-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d26d6-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="d26d6-127">Se resuelve un grupo de clases de mensajes en sus formularios en un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.</span><span class="sxs-lookup"><span data-stu-id="d26d6-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="d26d6-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d26d6-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="d26d6-129">Devuelve una matriz de las propiedades de todos los formularios instalados en un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d26d6-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="d26d6-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="d26d6-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="d26d6-131">Devuelve el nombre para mostrar de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d26d6-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="d26d6-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="d26d6-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="d26d6-133">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen en el objeto de contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d26d6-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d26d6-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="d26d6-134">See also</span></span>



[<span data-ttu-id="d26d6-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d26d6-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

