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
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817345"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="13f26-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="13f26-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="13f26-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13f26-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13f26-105">Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto de contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="13f26-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="13f26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13f26-106">Parameters</span></span>

 <span data-ttu-id="13f26-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="13f26-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="13f26-108">[entrada] Identificador de la ventana principal del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="13f26-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="13f26-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13f26-109">_ulFlags_</span></span>
  
> <span data-ttu-id="13f26-110">[entrada] Una máscara de bits de indicadores que controla cómo se selecciona la biblioteca de formularios (es decir, cómo el contenedor de formulario está seleccionado).</span><span class="sxs-lookup"><span data-stu-id="13f26-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="13f26-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="13f26-111">The following flags can be set:</span></span>
    
<span data-ttu-id="13f26-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="13f26-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="13f26-113">Selección se puede realizar desde todos los contenedores.</span><span class="sxs-lookup"><span data-stu-id="13f26-113">Selection can be made from all containers.</span></span> <span data-ttu-id="13f26-114">Éste es el tipo de selección de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="13f26-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="13f26-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="13f26-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="13f26-116">Selección puede realizarse sólo de los contenedores de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="13f26-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="13f26-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="13f26-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="13f26-118">Selección puede realizarse sólo de los contenedores que no estén asociados con las carpetas.</span><span class="sxs-lookup"><span data-stu-id="13f26-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="13f26-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="13f26-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="13f26-120">[out] Un puntero a un puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="13f26-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="13f26-121">Esta interfaz es para el objeto de contenedor que se ha seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="13f26-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13f26-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13f26-122">Return value</span></span>

<span data-ttu-id="13f26-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="13f26-123">S_OK</span></span> 
  
> <span data-ttu-id="13f26-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="13f26-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13f26-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13f26-125">Remarks</span></span>

<span data-ttu-id="13f26-126">Visores de formulario normalmente llama al método de **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario en el que está instalado un formulario.</span><span class="sxs-lookup"><span data-stu-id="13f26-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="13f26-127">**SelectFormContainer** no se puede usar para seleccionar el contenedor de forma local, que tiene el valor HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="13f26-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="13f26-128">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="13f26-128">MFCMAPI reference</span></span>

<span data-ttu-id="13f26-129">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="13f26-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13f26-130">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="13f26-130">**File**</span></span>|<span data-ttu-id="13f26-131">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="13f26-131">**Function**</span></span>|<span data-ttu-id="13f26-132">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="13f26-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13f26-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="13f26-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="13f26-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="13f26-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="13f26-135">MFCMAPI usa el método **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario antes de representar su contenido.</span><span class="sxs-lookup"><span data-stu-id="13f26-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13f26-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="13f26-136">See also</span></span>



[<span data-ttu-id="13f26-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13f26-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="13f26-138">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="13f26-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

