---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 06341f897a7865c09a565db67bb409fc9f49f8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817498"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="35b74-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="35b74-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="35b74-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35b74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35b74-105">Muestra una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="35b74-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="35b74-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35b74-106">Parameters</span></span>

 <span data-ttu-id="35b74-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="35b74-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="35b74-108">[entrada] Identificador de la ventana principal de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="35b74-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="35b74-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35b74-109">_ulFlags_</span></span>
  
> <span data-ttu-id="35b74-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="35b74-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="35b74-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="35b74-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="35b74-112">[entrada] Un puntero al título de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="35b74-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="35b74-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="35b74-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="35b74-114">[entrada] Un puntero a la tabla de presentación que se describe los controles para que aparezca en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="35b74-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="35b74-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="35b74-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="35b74-116">[entrada] Un puntero a la implementación de [IMAPIProp](imapipropiunknown.md) que se usará para obtener acceso a las propiedades de configuración que se mostrará en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="35b74-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="35b74-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="35b74-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="35b74-118">[entrada] Un índice basado en cero a la página superior predeterminada de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="35b74-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35b74-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35b74-119">Return value</span></span>

<span data-ttu-id="35b74-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="35b74-120">S_OK</span></span> 
  
> <span data-ttu-id="35b74-121">Se muestra la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="35b74-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35b74-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35b74-122">Remarks</span></span>

<span data-ttu-id="35b74-123">El método **IMAPISupport::DoConfigPropsheet** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="35b74-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="35b74-124">**DoConfigPropSheet** proporciona una interfaz de usuario estándar para mostrar las propiedades de los proveedores de servicio y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="35b74-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="35b74-125">Debe utilizar este cuadro de diálogo estándar para todas las pantallas de propiedad de configuración para que los usuarios se benefician de una interfaz coherente de Windows.</span><span class="sxs-lookup"><span data-stu-id="35b74-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="35b74-126">Proveedores de servicios de llamada **DoConfigPropSheet** como parte de su implementación del método [SettingsDialog](imapistatus-settingsdialog.md) o desde un botón que se utiliza para mostrar detalles en Propiedades.</span><span class="sxs-lookup"><span data-stu-id="35b74-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="35b74-127">Servicios de mensajes, llamar a **DoConfigPropSheet** desde su función de punto de entrada de servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="35b74-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="35b74-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="35b74-128">Notes to callers</span></span>

<span data-ttu-id="35b74-129">Puede crear la tabla de presentación indicada por el parámetro _lpDisplayTable_ mediante una llamada a la función [BuildDisplayTable](builddisplaytable.md) o con código personalizado.</span><span class="sxs-lookup"><span data-stu-id="35b74-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35b74-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="35b74-130">See also</span></span>



[<span data-ttu-id="35b74-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="35b74-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="35b74-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="35b74-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="35b74-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="35b74-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="35b74-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35b74-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="35b74-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="35b74-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="35b74-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35b74-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="35b74-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="35b74-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="35b74-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="35b74-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="35b74-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="35b74-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

