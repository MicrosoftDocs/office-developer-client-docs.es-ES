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
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577929"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="c3767-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="c3767-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="c3767-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3767-105">Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto de contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c3767-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="c3767-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3767-106">Parameters</span></span>

 <span data-ttu-id="c3767-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c3767-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c3767-108">[entrada] Identificador de la ventana principal del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="c3767-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="c3767-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3767-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c3767-110">[entrada] Una máscara de bits de indicadores que controla cómo se selecciona la biblioteca de formularios (es decir, cómo el contenedor de formulario está seleccionado).</span><span class="sxs-lookup"><span data-stu-id="c3767-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="c3767-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c3767-111">The following flags can be set:</span></span>
    
<span data-ttu-id="c3767-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="c3767-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="c3767-113">Selección se puede realizar desde todos los contenedores.</span><span class="sxs-lookup"><span data-stu-id="c3767-113">Selection can be made from all containers.</span></span> <span data-ttu-id="c3767-114">Éste es el tipo de selección de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c3767-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="c3767-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="c3767-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="c3767-116">Selección puede realizarse sólo de los contenedores de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c3767-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="c3767-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="c3767-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="c3767-118">Selección puede realizarse sólo de los contenedores que no estén asociados con las carpetas.</span><span class="sxs-lookup"><span data-stu-id="c3767-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="c3767-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="c3767-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="c3767-120">[out] Un puntero a un puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="c3767-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="c3767-121">Esta interfaz es para el objeto de contenedor que se ha seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c3767-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c3767-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3767-122">Return value</span></span>

<span data-ttu-id="c3767-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3767-123">S_OK</span></span> 
  
> <span data-ttu-id="c3767-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="c3767-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3767-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3767-125">Remarks</span></span>

<span data-ttu-id="c3767-126">Visores de formulario normalmente llama al método de **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario en el que está instalado un formulario.</span><span class="sxs-lookup"><span data-stu-id="c3767-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="c3767-127">**SelectFormContainer** no se puede usar para seleccionar el contenedor de forma local, que tiene el valor HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="c3767-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3767-128">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c3767-128">MFCMAPI reference</span></span>

<span data-ttu-id="c3767-129">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c3767-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3767-130">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="c3767-130">**File**</span></span>|<span data-ttu-id="c3767-131">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="c3767-131">**Function**</span></span>|<span data-ttu-id="c3767-132">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c3767-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3767-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c3767-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="c3767-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="c3767-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="c3767-135">MFCMAPI usa el método **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario antes de representar su contenido.</span><span class="sxs-lookup"><span data-stu-id="c3767-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3767-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c3767-136">See also</span></span>



[<span data-ttu-id="c3767-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3767-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="c3767-138">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c3767-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

