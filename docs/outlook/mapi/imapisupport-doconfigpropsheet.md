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
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra una hoja de propiedades de configuración.
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal de la hoja de propiedades.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpszTitle_
  
> [in] Puntero al título de la hoja de propiedades.
    
 _lpDisplayTable_
  
> [in] Puntero a la tabla para mostrar que describe los controles que aparecen en la hoja de propiedades.
    
 _lpConfigData_
  
> [in] Puntero a la implementación [de IMAPIProp](imapipropiunknown.md) que se usará para obtener acceso a las propiedades de configuración que se mostrarán en la hoja de propiedades. 
    
 _ulTopPage_
  
> [in] Índice basado en cero en la página superior predeterminada de la hoja de propiedades.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha mostrado la hoja de propiedades de configuración.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::D oConfigPropsheet** se implementa para todos los objetos de soporte técnico. **DoConfigPropSheet proporciona** una interfaz de usuario estándar para mostrar las propiedades de los proveedores de servicios y los servicios de mensajes. Debe usar este cuadro de diálogo estándar para todas las pantallas de propiedades de configuración para que los usuarios se beneficien de una interfaz Windows coherente. 
  
Los proveedores de servicios llaman a **DoConfigPropSheet** como parte de la implementación del método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) o desde un botón usado para mostrar detalles sobre las propiedades. Los servicios de mensajes **llaman a DoConfigPropSheet** desde su función de punto de entrada de servicio de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede crear la tabla para mostrar a la que apunta el parámetro  _lpDisplayTable_ llamando a la [función BuildDisplayTable](builddisplaytable.md) o con código personalizado. 
  
## <a name="see-also"></a>Vea también



[BuildDisplayTable](builddisplaytable.md)
  
[CreateIProp](createiprop.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

