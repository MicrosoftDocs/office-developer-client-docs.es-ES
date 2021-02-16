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
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430808"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un proveedor de servicios al servicio de mensajes. 
  
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
  
> [entrada] Puntero al nombre del proveedor que se agregará.
    
 _cValues_
  
> [entrada] Recuento de valores de propiedad a los que apunta el _parámetro lpProps._ 
    
 _lpProps_
  
> [entrada] Puntero a una matriz de valores de propiedad que describe las propiedades del proveedor que se agregarán.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestra este método. El _parámetro ulUIParam_ se usa si la MAPI_DIALOG se establece en el _parámetro ulFlags._ 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la adición del proveedor. Se pueden establecer las siguientes marcas:
    
  - MAPI_DIALOG: muestra un cuadro de diálogo para solicitar información de configuración.
      
  - MAPI_UNICODE: el nombre del proveedor y las propiedades de cadena están en formato Unicode. Si no MAPI_UNICODE marca, estas cadenas están en formato ANSI.
    
 _lpUID_
  
> [salida] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa el proveedor que se debe agregar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor se agregó correctamente al servicio de mensajes.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IProviderAdmin::CreateProvider** agrega un proveedor de servicios al servicio de mensajes. El  _parámetro lpszProvider_ debe apuntar al nombre de un proveedor que pertenece al servicio de mensajes. **CreateProvider** no comprueba si el nombre coincide con el nombre de un proveedor en el servicio; si el nombre pasado no coincide con un nombre de servicio, la llamada se realiza correctamente, pero los resultados son impredecibles. La mayoría de los servicios de mensajes no permiten agregar ni eliminar proveedores mientras el perfil está en uso. 
  
Después de agregar toda la información disponible sobre el proveedor de servicios al perfil desde el archivo Mapisvc.inf, **CreateProvider** llama a la función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_PROVIDER_CREATE. Si MAPI_DIALOG se establece en el parámetro _ulFlags_ del método **CreateProvider,** los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada. Estos parámetros adicionales permiten al proveedor de servicios mostrar su hoja de propiedades para que el usuario pueda especificar las opciones de configuración. 
  
## <a name="see-also"></a>Consulte también

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

