---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420314"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="34c99-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="34c99-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="34c99-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34c99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34c99-105">Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de objetos de información de formulario que describen dichos formularios.</span><span class="sxs-lookup"><span data-stu-id="34c99-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="34c99-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="34c99-106">Parameters</span></span>

 <span data-ttu-id="34c99-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="34c99-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="34c99-108">[in] Identificador de la ventana principal del cuadro de diálogo mostrado.</span><span class="sxs-lookup"><span data-stu-id="34c99-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="34c99-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34c99-109">_ulFlags_</span></span>
  
> <span data-ttu-id="34c99-110">[in] Máscara de bits de marcas que controla el tipo de las cadenas pasadas.</span><span class="sxs-lookup"><span data-stu-id="34c99-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="34c99-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="34c99-111">The following flag can be set:</span></span>
    
<span data-ttu-id="34c99-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="34c99-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="34c99-113">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="34c99-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="34c99-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="34c99-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="34c99-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="34c99-115">_pszTitle_</span></span>
  
> <span data-ttu-id="34c99-116">[in] Puntero a una cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="34c99-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="34c99-117">Si el  _parámetro pszTitle_ es NULL, el proveedor de biblioteca de formularios que proporciona los formularios proporciona un título predeterminado.</span><span class="sxs-lookup"><span data-stu-id="34c99-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="34c99-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="34c99-118">_pfld_</span></span>
  
> <span data-ttu-id="34c99-119">[in] Puntero a la carpeta desde la que se seleccionan los formularios.</span><span class="sxs-lookup"><span data-stu-id="34c99-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="34c99-120">Si el  _parámetro pfld_ es NULL, los formularios se seleccionan desde el contenedor de formularios local, personal u organización.</span><span class="sxs-lookup"><span data-stu-id="34c99-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="34c99-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="34c99-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="34c99-122">[in] Puntero a una matriz de objetos de información de formulario que están preseleccionados para el usuario.</span><span class="sxs-lookup"><span data-stu-id="34c99-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="34c99-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="34c99-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="34c99-124">[salida] Puntero a un puntero a la matriz devuelta de objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="34c99-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34c99-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34c99-125">Return value</span></span>

<span data-ttu-id="34c99-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="34c99-126">S_OK</span></span> 
  
> <span data-ttu-id="34c99-127">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="34c99-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="34c99-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="34c99-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="34c99-129">La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="34c99-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="34c99-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="34c99-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="34c99-131">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="34c99-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34c99-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34c99-132">Remarks</span></span>

<span data-ttu-id="34c99-133">Los visores de formularios llaman al método **IMAPIFormMgr::SelectMultipleForms** para presentar primero un cuadro de diálogo que permite al usuario seleccionar varios formularios y, a continuación, recuperar una matriz de objetos de información de formulario que describen los formularios seleccionados.</span><span class="sxs-lookup"><span data-stu-id="34c99-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="34c99-134">El **cuadro de diálogo SelectMultipleForms** muestra todos los formularios, independientemente de si están ocultos (es decir, si sus propiedades ocultas están o no claras).</span><span class="sxs-lookup"><span data-stu-id="34c99-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="34c99-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="34c99-135">Notes to implementers</span></span>

<span data-ttu-id="34c99-136">Si un visor de formulario pasa la marca MAPI_UNICODE en el  _parámetro ulFlags,_ todas las cadenas son Unicode.</span><span class="sxs-lookup"><span data-stu-id="34c99-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="34c99-137">Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa.</span><span class="sxs-lookup"><span data-stu-id="34c99-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34c99-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="34c99-138">See also</span></span>



[<span data-ttu-id="34c99-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34c99-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

