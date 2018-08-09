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
ms.openlocfilehash: fa439d0a6fa59bac787f09c3f894a750948a0a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817295"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="9e6ba-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9e6ba-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="9e6ba-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e6ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e6ba-105">Proporciona acceso de las aplicaciones de cliente a las propiedades que son específicas de la definición del formulario.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="9e6ba-106">Al mantener la información del formulario en un objeto independiente, el proveedor de la biblioteca de formulario puede describir un formulario a un cliente sin activar el formulario.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e6ba-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-107">Header file:</span></span>  <br/> |<span data-ttu-id="9e6ba-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="9e6ba-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9e6ba-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="9e6ba-110">Objetos de información de formulario</span><span class="sxs-lookup"><span data-stu-id="9e6ba-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="9e6ba-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e6ba-112">Proveedores de biblioteca de formulario</span><span class="sxs-lookup"><span data-stu-id="9e6ba-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="9e6ba-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-113">Called by:</span></span>  <br/> |<span data-ttu-id="9e6ba-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="9e6ba-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="9e6ba-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9e6ba-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="9e6ba-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="9e6ba-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="9e6ba-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="9e6ba-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="9e6ba-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="9e6ba-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="9e6ba-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="9e6ba-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9e6ba-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="9e6ba-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9e6ba-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9e6ba-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="9e6ba-123">Devuelve un puntero a todo el conjunto de propiedades que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="9e6ba-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="9e6ba-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="9e6ba-125">Devuelve un puntero a todo el conjunto de verbos que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="9e6ba-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="9e6ba-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="9e6ba-127">Se basa en un icono de una propiedad de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="9e6ba-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="9e6ba-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="9e6ba-129">Guarda una descripción de un formulario determinado en un archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="9e6ba-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="9e6ba-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="9e6ba-131">Devuelve un puntero al contenedor de formulario en el que está instalado un formulario en particular.</span><span class="sxs-lookup"><span data-stu-id="9e6ba-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e6ba-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e6ba-132">Remarks</span></span>

<span data-ttu-id="9e6ba-133">A diferencia de la mayoría de las interfaces definida en el archivo de encabezado MapiForm.h, **IMAPIFormInfo** se hereda de la interfaz [IMAPIProp](imapipropiunknown.md) , debido a que exporta la mayoría información de formulario a través de las llamadas al método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6ba-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e6ba-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e6ba-134">See also</span></span>



[<span data-ttu-id="9e6ba-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9e6ba-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

