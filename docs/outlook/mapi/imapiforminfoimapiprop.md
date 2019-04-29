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
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417367"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="236f1-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="236f1-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="236f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="236f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="236f1-105">Proporciona a las aplicaciones cliente acceso a las propiedades que son específicas de la definición del formulario.</span><span class="sxs-lookup"><span data-stu-id="236f1-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="236f1-106">Al mantener la información del formulario en un objeto independiente, el proveedor de la biblioteca de formularios puede describir un formulario para un cliente sin activar el formulario.</span><span class="sxs-lookup"><span data-stu-id="236f1-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="236f1-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="236f1-107">Header file:</span></span>  <br/> |<span data-ttu-id="236f1-108">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="236f1-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="236f1-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="236f1-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="236f1-110">Objetos de información de formulario</span><span class="sxs-lookup"><span data-stu-id="236f1-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="236f1-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="236f1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="236f1-112">Proveedores de bibliotecas de formularios</span><span class="sxs-lookup"><span data-stu-id="236f1-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="236f1-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="236f1-113">Called by:</span></span>  <br/> |<span data-ttu-id="236f1-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="236f1-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="236f1-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="236f1-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="236f1-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="236f1-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="236f1-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="236f1-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="236f1-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="236f1-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="236f1-119">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="236f1-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="236f1-120">No transactd</span><span class="sxs-lookup"><span data-stu-id="236f1-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="236f1-121">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="236f1-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="236f1-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="236f1-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="236f1-123">Devuelve un puntero al conjunto completo de propiedades que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="236f1-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="236f1-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="236f1-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="236f1-125">Devuelve un puntero al conjunto completo de verbos que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="236f1-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="236f1-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="236f1-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="236f1-127">Crea un icono a partir de una propiedad Icon de un formulario.</span><span class="sxs-lookup"><span data-stu-id="236f1-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="236f1-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="236f1-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="236f1-129">Guarda una descripción de un formulario en particular en un archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="236f1-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="236f1-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="236f1-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="236f1-131">Devuelve un puntero al contenedor de formularios en el que se instala un formulario determinado.</span><span class="sxs-lookup"><span data-stu-id="236f1-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="236f1-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="236f1-132">Remarks</span></span>

<span data-ttu-id="236f1-133">A diferencia de la mayoría de las interfaces definidas en el archivo de encabezado MapiForm. h, **IMAPIFormInfo** hereda de la interfaz [IMAPIProp](imapipropiunknown.md) , porque exporta la mayoría de la información de formulario mediante llamadas al método [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="236f1-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="236f1-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="236f1-134">See also</span></span>



[<span data-ttu-id="236f1-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="236f1-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

