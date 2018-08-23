---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bf3d9159dd1ed31fb93569218770f1015579339
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582927"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="39b5f-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="39b5f-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="39b5f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39b5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39b5f-105">Se abre una interfaz de [IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de forma específicos.</span><span class="sxs-lookup"><span data-stu-id="39b5f-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="39b5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39b5f-106">Parameters</span></span>

 <span data-ttu-id="39b5f-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="39b5f-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="39b5f-108">[entrada] Una enumeración HFRMREG que indica la biblioteca de formularios para abrir (es decir, el contenedor de formulario para abrir).</span><span class="sxs-lookup"><span data-stu-id="39b5f-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="39b5f-109">Una enumeración HFRMREG es una enumeración que es específica de un proveedor de la biblioteca de formulario.</span><span class="sxs-lookup"><span data-stu-id="39b5f-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="39b5f-110">Los valores posibles de HFRMREG incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="39b5f-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="39b5f-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="39b5f-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="39b5f-112">Un contenedor conveniente formulario.</span><span class="sxs-lookup"><span data-stu-id="39b5f-112">A convenient form container.</span></span>
    
<span data-ttu-id="39b5f-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="39b5f-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="39b5f-114">Un contenedor de carpeta.</span><span class="sxs-lookup"><span data-stu-id="39b5f-114">A folder container.</span></span> 
    
<span data-ttu-id="39b5f-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="39b5f-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="39b5f-116">El contenedor para el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="39b5f-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="39b5f-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="39b5f-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="39b5f-118">Un contenedor de forma local.</span><span class="sxs-lookup"><span data-stu-id="39b5f-118">A local form container.</span></span> 
    
 <span data-ttu-id="39b5f-119">_lpUnk_</span><span class="sxs-lookup"><span data-stu-id="39b5f-119">_lpunk_</span></span>
  
> <span data-ttu-id="39b5f-120">[entrada] Un puntero al objeto para el que se abre la interfaz.</span><span class="sxs-lookup"><span data-stu-id="39b5f-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="39b5f-121">El parámetro _lpunk_ debe ser **null** a menos que el valor para el parámetro _hfrmreg_ requiere un puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="39b5f-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="39b5f-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="39b5f-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="39b5f-123">[out] Un puntero a un puntero al objeto de contenedor de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="39b5f-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39b5f-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39b5f-124">Return value</span></span>

<span data-ttu-id="39b5f-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="39b5f-125">S_OK</span></span> 
  
> <span data-ttu-id="39b5f-126">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="39b5f-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="39b5f-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="39b5f-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="39b5f-128">El objeto al que señala por _lpunk_ no es compatible con la interfaz necesaria.</span><span class="sxs-lookup"><span data-stu-id="39b5f-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39b5f-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39b5f-129">Remarks</span></span>

<span data-ttu-id="39b5f-130">Visores de formulario llamar al método **IMAPIFormMgr::OpenFormContainer** para abrir una interfaz **IMAPIFormContainer** para un contenedor de forma específicos.</span><span class="sxs-lookup"><span data-stu-id="39b5f-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="39b5f-131">A continuación, se puede usar esta interfaz para instalar formularios en y formularios de eliminación de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="39b5f-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="39b5f-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="39b5f-132">Notes to callers</span></span>

<span data-ttu-id="39b5f-133">Si el valor de _hfrmreg_ es HFRMREG_FOLDER, el identificador de interfaz que se usa en _lpunk_ debe ser distinto de **null** y debe permitir llamadas al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) a una interfaz [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="39b5f-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="39b5f-134">Para abrir el contenedor de forma local, debe usar una llamada al método **OpenFormContainer** o la función [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; no puede usar el método [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir que el usuario seleccionar el contenedor de forma local.</span><span class="sxs-lookup"><span data-stu-id="39b5f-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="39b5f-135">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="39b5f-135">MFCMAPI reference</span></span>

<span data-ttu-id="39b5f-136">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="39b5f-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="39b5f-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="39b5f-137">**File**</span></span>|<span data-ttu-id="39b5f-138">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="39b5f-138">**Function**</span></span>|<span data-ttu-id="39b5f-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="39b5f-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39b5f-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="39b5f-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="39b5f-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="39b5f-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="39b5f-142">MFCMAPI usa el método **IMAPIFormMgr::OpenFormContainer** para recuperar un contenedor de formulario por lo que se puede representar el contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="39b5f-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="39b5f-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="39b5f-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="39b5f-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="39b5f-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="39b5f-145">MFCMAPI usa el método **IMAPIFormMgr::OpenFormContainer** para recuperar un contenedor de formulario para una carpeta, por lo que se puede representar el contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="39b5f-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39b5f-146">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="39b5f-146">See also</span></span>



[<span data-ttu-id="39b5f-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="39b5f-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="39b5f-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="39b5f-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="39b5f-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="39b5f-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="39b5f-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39b5f-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="39b5f-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="39b5f-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

