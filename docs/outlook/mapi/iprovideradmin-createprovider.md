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

## <a name="parameters"></a>Parameters

 _lpszProvider_
  
> a Un puntero al nombre del proveedor que se va a agregar.
    
 _cValues_
  
> a El número de valores de propiedad a los que apunta el parámetro _lpProps_ . 
    
 _lpProps_
  
> a Un puntero a una matriz de valores de propiedad que describe las propiedades del proveedor que se va a agregar.
    
 _ulUIParam_
  
> a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra. El parámetro _ulUIParam_ se usa si la marca MAPI_DIALOG se establece en el parámetro _ulFlags_ . 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la adición del proveedor. Se pueden establecer los siguientes indicadores:
    
  - MAPI_DIALOG: muestra un cuadro de diálogo para solicitar información de configuración.
      
  - MAPI_UNICODE: el nombre del proveedor y las propiedades de la cadena están en formato Unicode. Si no se establece la marca MAPI_UNICODE, estas cadenas están en formato ANSI.
    
 _lpUID_
  
> contempla Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa al proveedor que se va a agregar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor se agregó correctamente al servicio de mensajes.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin:: CreateProvider** agrega un proveedor de servicios al servicio de mensajes. El parámetro _lpszProvider_ debe apuntar al nombre de un proveedor que pertenezca al servicio de mensajes. **CreateProvider** no comprueba si el nombre coincide con el nombre de un proveedor en el servicio; Si el nombre pasado no coincide con un nombre de servicio, la llamada se realiza correctamente, pero los resultados son imprevisibles. La mayoría de los servicios de mensajes no permiten que se agreguen o eliminen proveedores mientras el perfil está en uso. 
  
Una vez que se ha agregado al perfil toda la información disponible sobre el proveedor de servicios desde el archivo MAPISVC. inf, **CreateProvider** llama a la función de punto de entrada del servicio de mensajería con el parámetro _ULCONTEXT_ establecido en MSG_SERVICE_ PROVIDER_CREATE. Si MAPI_DIALOG se establece en el parámetro _ulFlags_ del método **CreateProvider** , los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada. Estos parámetros adicionales permiten al proveedor de servicios mostrar su hoja de propiedades para que el usuario pueda especificar las opciones de configuración. 
  
## <a name="see-also"></a>Ver también

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

