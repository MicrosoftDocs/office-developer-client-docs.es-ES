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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817328"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="c4f0b-103">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4f0b-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="c4f0b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4f0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4f0b-105">Permite que los visores de formulario obtener información acerca de y activar servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4f0b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c4f0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4f0b-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="c4f0b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="c4f0b-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="c4f0b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c4f0b-109">Objetos de administrador de formulario</span><span class="sxs-lookup"><span data-stu-id="c4f0b-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="c4f0b-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c4f0b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4f0b-111">Proveedores de biblioteca de formulario</span><span class="sxs-lookup"><span data-stu-id="c4f0b-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="c4f0b-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c4f0b-112">Called by:</span></span>  <br/> |<span data-ttu-id="c4f0b-113">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="c4f0b-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="c4f0b-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="c4f0b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c4f0b-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="c4f0b-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="c4f0b-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="c4f0b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c4f0b-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="c4f0b-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c4f0b-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="c4f0b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c4f0b-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="c4f0b-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="c4f0b-120">Inicia un formulario para abrir un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="c4f0b-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="c4f0b-122">Una clase de mensaje se resuelve en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c4f0b-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="c4f0b-124">Se resuelve un grupo de clases de mensajes en sus formularios dentro de un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c4f0b-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="c4f0b-126">Devuelve una matriz de las propiedades que utiliza un grupo de formularios.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="c4f0b-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="c4f0b-128">Inicia un formulario para crear un nuevo mensaje en función de la clase de mensaje del formulario.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="c4f0b-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="c4f0b-130">Presenta un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe ese formulario.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="c4f0b-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="c4f0b-132">Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de formulario objetos de información que se describen dichos formularios.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="c4f0b-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="c4f0b-134">Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto de contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="c4f0b-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="c4f0b-136">Se abre una interfaz de [IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de forma específicos.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="c4f0b-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="c4f0b-138">Descargas de un formulario para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="c4f0b-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="c4f0b-140">Determina si un formulario puede controlar sus propio conflictos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="c4f0b-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="c4f0b-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="c4f0b-142">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen en el objeto de administrador de formulario.</span><span class="sxs-lookup"><span data-stu-id="c4f0b-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4f0b-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="c4f0b-143">See also</span></span>



[<span data-ttu-id="c4f0b-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c4f0b-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

