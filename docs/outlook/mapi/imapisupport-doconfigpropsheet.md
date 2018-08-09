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
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Hace referencia a**: Outlook 
  
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

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de la hoja de propiedades.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpszTitle_
  
> [entrada] Un puntero al título de la hoja de propiedades.
    
 _lpDisplayTable_
  
> [entrada] Un puntero a la tabla de presentación que se describe los controles para que aparezca en la hoja de propiedades.
    
 _lpConfigData_
  
> [entrada] Un puntero a la implementación de [IMAPIProp](imapipropiunknown.md) que se usará para obtener acceso a las propiedades de configuración que se mostrará en la hoja de propiedades. 
    
 _ulTopPage_
  
> [entrada] Un índice basado en cero a la página superior predeterminada de la hoja de propiedades.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se muestra la hoja de propiedades de configuración.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::DoConfigPropsheet** se implementa para todos los objetos de soporte técnico. **DoConfigPropSheet** proporciona una interfaz de usuario estándar para mostrar las propiedades de los proveedores de servicio y servicios de mensajes. Debe utilizar este cuadro de diálogo estándar para todas las pantallas de propiedad de configuración para que los usuarios se benefician de una interfaz coherente de Windows. 
  
Proveedores de servicios de llamada **DoConfigPropSheet** como parte de su implementación del método [SettingsDialog](imapistatus-settingsdialog.md) o desde un botón que se utiliza para mostrar detalles en Propiedades. Servicios de mensajes, llamar a **DoConfigPropSheet** desde su función de punto de entrada de servicio de mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede crear la tabla de presentación indicada por el parámetro _lpDisplayTable_ mediante una llamada a la función [BuildDisplayTable](builddisplaytable.md) o con código personalizado. 
  
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

