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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322375"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="761ef-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="761ef-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="761ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="761ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="761ef-105">Muestra una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="761ef-105">Displays a configuration property sheet.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="761ef-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="761ef-106">Parameters</span></span>

 <span data-ttu-id="761ef-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="761ef-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="761ef-108">a Identificador de la ventana primaria de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="761ef-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="761ef-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="761ef-109">_ulFlags_</span></span>
  
> <span data-ttu-id="761ef-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="761ef-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="761ef-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="761ef-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="761ef-112">a Un puntero al título de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="761ef-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="761ef-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="761ef-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="761ef-114">a Un puntero a la tabla de presentación que describe los controles que deben aparecer en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="761ef-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="761ef-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="761ef-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="761ef-116">a Un puntero a la implementación de [IMAPIProp](imapipropiunknown.md) que se va a usar para obtener acceso a las propiedades de configuración que se mostrarán en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="761ef-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="761ef-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="761ef-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="761ef-118">a Índice de base cero de la página superior predeterminada de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="761ef-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="761ef-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="761ef-119">Return value</span></span>

<span data-ttu-id="761ef-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="761ef-120">S_OK</span></span> 
  
> <span data-ttu-id="761ef-121">Se muestra la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="761ef-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="761ef-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="761ef-122">Remarks</span></span>

<span data-ttu-id="761ef-123">El método **IMAPISupport::D oconfigpropsheet** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="761ef-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="761ef-124">**DoConfigPropSheet** proporciona una interfaz de usuario estándar para mostrar las propiedades de los proveedores de servicios y los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="761ef-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="761ef-125">Debe usar este cuadro de diálogo estándar para todas las pantallas de propiedades de configuración para que los usuarios se beneficien de una interfaz de Windows coherente.</span><span class="sxs-lookup"><span data-stu-id="761ef-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="761ef-126">Los proveedores de servicios llaman a **DoConfigPropSheet** como parte de su implementación del método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) o desde un botón usado para mostrar detalles sobre las propiedades.</span><span class="sxs-lookup"><span data-stu-id="761ef-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="761ef-127">Los servicios de mensajes llaman a **DoConfigPropSheet** desde su función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="761ef-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="761ef-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="761ef-128">Notes to callers</span></span>

<span data-ttu-id="761ef-129">Puede crear la tabla de presentación a la que señala el parámetro _lpDisplayTable_ llamando a la función [BuildDisplayTable](builddisplaytable.md) o con código personalizado.</span><span class="sxs-lookup"><span data-stu-id="761ef-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="761ef-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="761ef-130">See also</span></span>



[<span data-ttu-id="761ef-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="761ef-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="761ef-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="761ef-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="761ef-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="761ef-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="761ef-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="761ef-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="761ef-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="761ef-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="761ef-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="761ef-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="761ef-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="761ef-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="761ef-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="761ef-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="761ef-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="761ef-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

