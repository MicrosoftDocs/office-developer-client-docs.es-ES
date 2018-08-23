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
ms.openlocfilehash: b974b733c24e61cb256ac0cf7b377d5630966fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579294"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="474b0-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="474b0-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="474b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="474b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="474b0-105">Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de formulario objetos de información que se describen dichos formularios.</span><span class="sxs-lookup"><span data-stu-id="474b0-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="474b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="474b0-106">Parameters</span></span>

 <span data-ttu-id="474b0-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="474b0-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="474b0-108">[entrada] Identificador de la ventana principal del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="474b0-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="474b0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="474b0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="474b0-110">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas que se pasan en.</span><span class="sxs-lookup"><span data-stu-id="474b0-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="474b0-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="474b0-111">The following flag can be set:</span></span>
    
<span data-ttu-id="474b0-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="474b0-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="474b0-113">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="474b0-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="474b0-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="474b0-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="474b0-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="474b0-115">_pszTitle_</span></span>
  
> <span data-ttu-id="474b0-116">[entrada] Un puntero a una cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="474b0-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="474b0-117">Si el parámetro _pszTitle_ es NULL, el proveedor de la biblioteca de formulario que proporciona los formularios proporciona un título predeterminado.</span><span class="sxs-lookup"><span data-stu-id="474b0-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="474b0-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="474b0-118">_pfld_</span></span>
  
> <span data-ttu-id="474b0-119">[entrada] Un puntero a la carpeta desde la que se va a seleccionar los formularios.</span><span class="sxs-lookup"><span data-stu-id="474b0-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="474b0-120">Si el parámetro _pfld_ es NULL, se seleccionan los formularios desde el contenedor de forma local, el personal o la organización.</span><span class="sxs-lookup"><span data-stu-id="474b0-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="474b0-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="474b0-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="474b0-122">[entrada] Un puntero a una matriz de objetos de información de formulario que se preseleccionado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="474b0-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="474b0-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="474b0-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="474b0-124">[out] Un puntero a un puntero a la matriz devuelta de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="474b0-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="474b0-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="474b0-125">Return value</span></span>

<span data-ttu-id="474b0-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="474b0-126">S_OK</span></span> 
  
> <span data-ttu-id="474b0-127">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="474b0-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="474b0-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="474b0-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="474b0-129">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="474b0-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="474b0-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="474b0-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="474b0-131">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="474b0-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="474b0-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="474b0-132">Remarks</span></span>

<span data-ttu-id="474b0-133">Visores de formulario llamar al método **IMAPIFormMgr::SelectMultipleForms** a presenta primero un cuadro de diálogo que permite al usuario seleccionar varios formularios y, a continuación, para recuperar una matriz de formulario de información de los objetos que se describen los formularios seleccionados.</span><span class="sxs-lookup"><span data-stu-id="474b0-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="474b0-134">El cuadro de diálogo **SelectMultipleForms** muestra todos los formularios, independientemente de si están ocultos (es decir, si sus propiedades ocultas son claros).</span><span class="sxs-lookup"><span data-stu-id="474b0-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="474b0-135">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="474b0-135">Notes to implementers</span></span>

<span data-ttu-id="474b0-136">Si un visor de formulario, pasa el indicador MAPI_UNICODE el parámetro _ulFlags_ , todas las cadenas son cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="474b0-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="474b0-137">Proveedores de biblioteca de formulario que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="474b0-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="474b0-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="474b0-138">See also</span></span>



[<span data-ttu-id="474b0-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="474b0-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

