---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428595"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="b0978-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="b0978-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="b0978-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0978-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0978-105">Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b0978-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="b0978-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b0978-106">Parameters</span></span>

 <span data-ttu-id="b0978-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b0978-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b0978-108">[in] Identificador de la ventana principal del cuadro de diálogo mostrado.</span><span class="sxs-lookup"><span data-stu-id="b0978-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="b0978-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0978-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b0978-110">[in] Máscara de bits de marcas que controla cómo se selecciona la biblioteca de formularios (es decir, cómo se selecciona el contenedor de formularios).</span><span class="sxs-lookup"><span data-stu-id="b0978-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="b0978-111">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="b0978-111">The following flags can be set:</span></span>
    
<span data-ttu-id="b0978-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="b0978-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="b0978-113">La selección se puede realizar desde todos los contenedores.</span><span class="sxs-lookup"><span data-stu-id="b0978-113">Selection can be made from all containers.</span></span> <span data-ttu-id="b0978-114">Este es el tipo de selección predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b0978-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="b0978-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="b0978-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="b0978-116">La selección solo se puede realizar desde contenedores de carpetas.</span><span class="sxs-lookup"><span data-stu-id="b0978-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="b0978-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="b0978-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="b0978-118">La selección solo se puede realizar desde contenedores que no están asociados con carpetas.</span><span class="sxs-lookup"><span data-stu-id="b0978-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="b0978-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="b0978-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="b0978-120">[salida] Puntero a un puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="b0978-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="b0978-121">Esta interfaz es para el objeto contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b0978-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0978-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0978-122">Return value</span></span>

<span data-ttu-id="b0978-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0978-123">S_OK</span></span> 
  
> <span data-ttu-id="b0978-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b0978-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0978-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0978-125">Remarks</span></span>

<span data-ttu-id="b0978-126">Los visores de formularios normalmente llaman al método **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario en el que está instalado un formulario.</span><span class="sxs-lookup"><span data-stu-id="b0978-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="b0978-127">**SelectFormContainer** no se puede usar para seleccionar el contenedor de formulario local, que tiene el valor HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="b0978-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b0978-128">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b0978-128">MFCMAPI reference</span></span>

<span data-ttu-id="b0978-129">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b0978-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b0978-130">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b0978-130">**File**</span></span>|<span data-ttu-id="b0978-131">**Función**</span><span class="sxs-lookup"><span data-stu-id="b0978-131">**Function**</span></span>|<span data-ttu-id="b0978-132">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b0978-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0978-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b0978-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b0978-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="b0978-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="b0978-135">MFCMAPI usa el **método IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario antes de representar su contenido.</span><span class="sxs-lookup"><span data-stu-id="b0978-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0978-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0978-136">See also</span></span>



[<span data-ttu-id="b0978-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0978-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="b0978-138">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b0978-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

