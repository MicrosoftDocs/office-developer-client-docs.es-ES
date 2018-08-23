---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575913"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="223bf-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="223bf-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="223bf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="223bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="223bf-105">Proporciona acceso de las aplicaciones de cliente a las propiedades que son específicas de la definición del formulario.</span><span class="sxs-lookup"><span data-stu-id="223bf-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="223bf-106">Al mantener la información del formulario en un objeto independiente, el proveedor de la biblioteca de formulario puede describir un formulario a un cliente sin activar el formulario.</span><span class="sxs-lookup"><span data-stu-id="223bf-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="223bf-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="223bf-107">Header file:</span></span>  <br/> |<span data-ttu-id="223bf-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="223bf-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="223bf-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="223bf-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="223bf-110">Objetos de información de formulario</span><span class="sxs-lookup"><span data-stu-id="223bf-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="223bf-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="223bf-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="223bf-112">Proveedores de biblioteca de formulario</span><span class="sxs-lookup"><span data-stu-id="223bf-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="223bf-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="223bf-113">Called by:</span></span>  <br/> |<span data-ttu-id="223bf-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="223bf-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="223bf-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="223bf-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="223bf-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="223bf-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="223bf-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="223bf-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="223bf-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="223bf-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="223bf-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="223bf-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="223bf-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="223bf-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="223bf-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="223bf-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="223bf-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="223bf-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="223bf-123">Devuelve un puntero a todo el conjunto de propiedades que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="223bf-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="223bf-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="223bf-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="223bf-125">Devuelve un puntero a todo el conjunto de verbos que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="223bf-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="223bf-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="223bf-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="223bf-127">Se basa en un icono de una propiedad de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="223bf-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="223bf-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="223bf-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="223bf-129">Guarda una descripción de un formulario determinado en un archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="223bf-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="223bf-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="223bf-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="223bf-131">Devuelve un puntero al contenedor de formulario en el que está instalado un formulario en particular.</span><span class="sxs-lookup"><span data-stu-id="223bf-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="223bf-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="223bf-132">Remarks</span></span>

<span data-ttu-id="223bf-133">A diferencia de la mayoría de las interfaces definida en el archivo de encabezado MapiForm.h, **IMAPIFormInfo** se hereda de la interfaz [IMAPIProp](imapipropiunknown.md) , debido a que exporta la mayoría información de formulario a través de las llamadas al método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="223bf-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="223bf-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="223bf-134">See also</span></span>



[<span data-ttu-id="223bf-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="223bf-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

