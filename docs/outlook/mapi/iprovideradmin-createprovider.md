---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 01cc8a8a54137b72091abab3671c08b526ef9e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817926"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Hace referencia a**: Outlook 
  
Agrega un proveedor de servicios para el servicio de mensajes. 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>Parámetros

 _lpszProvider_
  
> [entrada] Un puntero en el nombre del proveedor que se va a agregar.
    
 _cValues_
  
> [entrada] El recuento de valores de la propiedad indicada por el parámetro _lpProps_ . 
    
 _lpProps_
  
> [entrada] Un puntero a una matriz de valor de propiedad que se describe las propiedades del proveedor que se va a agregar.
    
 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método. Si se establece la marca MAPI_DIALOG en el parámetro _ulFlags_ , se usa el parámetro _ulUIParam_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la adición de proveedor. Se pueden establecer los siguientes indicadores:
    
  - MAPI_DIALOG: Muestra un cuadro de diálogo para solicitar información de configuración.
      
  - MAPI_UNICODE.: Las propiedades de cadena y el nombre del proveedor están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.
    
 _lpUID_
  
> [out] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa el proveedor que se va a agregar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor se ha agregado correctamente al servicio de mensajes.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin::CreateProvider** agrega un proveedor de servicios para el servicio de mensajes. El parámetro _lpszProvider_ debe apuntar al nombre de un proveedor que pertenece al servicio de mensajes. **CreateProvider** no comprueba si el nombre coincide con el nombre de un proveedor en el servicio; Si el nombre pasado no coincide con un nombre de servicio, la llamada se realiza correctamente, pero los resultados serán impredecibles. La mayoría de los servicios de mensaje no permiten que los proveedores se agregan o eliminan mientras el perfil está en uso. 
  
Después de todo de la información disponible sobre el servicio de proveedor se ha agregado al perfil desde el archivo Mapisvc.inf, **CreateProvider** llama la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_ PROVIDER_CREATE. Si de MAPI_DIALOG se establece en el **CreateProvider** parámetro del método _ulFlags_ , los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada. Estos parámetros adicionales habilitar el proveedor de servicios mostrar su hoja de propiedades, por lo que el usuario puede escribir valores de configuración. 
  
## <a name="see-also"></a>Vea también

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

