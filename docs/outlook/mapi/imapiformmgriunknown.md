---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413062"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="48a20-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48a20-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="48a20-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48a20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48a20-105">Permite a los visores de formulario obtener información sobre y activar servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="48a20-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48a20-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="48a20-106">Header file:</span></span>  <br/> |<span data-ttu-id="48a20-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="48a20-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="48a20-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="48a20-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="48a20-109">Objetos del administrador de formularios</span><span class="sxs-lookup"><span data-stu-id="48a20-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="48a20-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="48a20-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="48a20-111">Proveedores de bibliotecas de formularios</span><span class="sxs-lookup"><span data-stu-id="48a20-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="48a20-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="48a20-112">Called by:</span></span>  <br/> |<span data-ttu-id="48a20-113">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="48a20-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="48a20-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="48a20-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="48a20-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="48a20-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="48a20-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="48a20-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="48a20-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="48a20-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="48a20-118">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="48a20-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="48a20-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="48a20-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="48a20-120">Inicia un formulario para abrir un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="48a20-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="48a20-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="48a20-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="48a20-122">Resuelve una clase de mensaje en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="48a20-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="48a20-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="48a20-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="48a20-124">Resuelve un grupo de clases de mensaje en sus formularios dentro de un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.</span><span class="sxs-lookup"><span data-stu-id="48a20-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="48a20-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="48a20-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="48a20-126">Devuelve una matriz de las propiedades que usa un grupo de formularios.</span><span class="sxs-lookup"><span data-stu-id="48a20-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="48a20-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="48a20-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="48a20-128">Inicia un formulario para crear un nuevo mensaje basado en la clase de mensaje del formulario.</span><span class="sxs-lookup"><span data-stu-id="48a20-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="48a20-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="48a20-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="48a20-130">Presenta un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe ese formulario.</span><span class="sxs-lookup"><span data-stu-id="48a20-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="48a20-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="48a20-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="48a20-132">Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de objetos de información de formulario que describen dichos formularios.</span><span class="sxs-lookup"><span data-stu-id="48a20-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="48a20-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="48a20-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="48a20-134">Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="48a20-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="48a20-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="48a20-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="48a20-136">Abre una [interfaz IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de formulario específico.</span><span class="sxs-lookup"><span data-stu-id="48a20-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="48a20-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="48a20-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="48a20-138">Descarga un formulario para su apertura.</span><span class="sxs-lookup"><span data-stu-id="48a20-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="48a20-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="48a20-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="48a20-140">Determina si un formulario puede controlar sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="48a20-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="48a20-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="48a20-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="48a20-142">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto del administrador de formularios.</span><span class="sxs-lookup"><span data-stu-id="48a20-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48a20-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="48a20-143">See also</span></span>



[<span data-ttu-id="48a20-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="48a20-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

