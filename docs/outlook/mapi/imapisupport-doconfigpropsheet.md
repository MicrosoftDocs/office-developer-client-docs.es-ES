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
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429021"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="bb7b3-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="bb7b3-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="bb7b3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb7b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb7b3-105">Muestra una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-105">Displays a configuration property sheet.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="bb7b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb7b3-106">Parameters</span></span>

 <span data-ttu-id="bb7b3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bb7b3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="bb7b3-108">[entrada] Identificador de la ventana primaria de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="bb7b3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb7b3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bb7b3-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="bb7b3-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="bb7b3-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="bb7b3-112">[entrada] Puntero al título de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="bb7b3-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="bb7b3-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="bb7b3-114">[entrada] Puntero a la tabla para mostrar que describe los controles que aparecen en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="bb7b3-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="bb7b3-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="bb7b3-116">[entrada] Puntero a la [implementación IMAPIProp](imapipropiunknown.md) que se usará para obtener acceso a las propiedades de configuración que se mostrarán en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="bb7b3-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="bb7b3-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="bb7b3-118">[entrada] Índice de base cero en la página superior predeterminada de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb7b3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb7b3-119">Return value</span></span>

<span data-ttu-id="bb7b3-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb7b3-120">S_OK</span></span> 
  
> <span data-ttu-id="bb7b3-121">Se ha mostrado la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb7b3-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb7b3-122">Remarks</span></span>

<span data-ttu-id="bb7b3-123">El **método IMAPISupport::D oConfigPropsheet** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="bb7b3-124">**DoConfigPropSheet proporciona** una interfaz de usuario estándar para mostrar las propiedades de los proveedores de servicios y los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="bb7b3-125">Debes usar este cuadro de diálogo estándar para todas las pantallas de propiedades de configuración para que los usuarios se beneficien de una interfaz de Windows coherente.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="bb7b3-126">Los proveedores de servicios llaman a **DoConfigPropSheet** como parte de su implementación del método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) o desde un botón usado para mostrar detalles sobre las propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="bb7b3-127">Los servicios de mensajes **llaman a DoConfigPropSheet desde** su función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bb7b3-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bb7b3-128">Notes to callers</span></span>

<span data-ttu-id="bb7b3-129">Puede crear la tabla para mostrar a la que apunta el parámetro  _lpDisplayTable_ llamando a la [función BuildDisplayTable](builddisplaytable.md) o con código personalizado.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb7b3-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb7b3-130">See also</span></span>



[<span data-ttu-id="bb7b3-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="bb7b3-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="bb7b3-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="bb7b3-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="bb7b3-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="bb7b3-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="bb7b3-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb7b3-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="bb7b3-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="bb7b3-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="bb7b3-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb7b3-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="bb7b3-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="bb7b3-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="bb7b3-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="bb7b3-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="bb7b3-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb7b3-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

