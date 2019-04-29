---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439733"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra una hoja de propiedades que permite al usuario cambiar la configuración de un proveedor de servicios este método no se admite en objetos de estado que implementa MAPI.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria de la hoja de propiedades de configuración.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla la presentación de la hoja de propiedades. Se puede establecer la siguiente marca:
    
UI_READONLY 
  
> Sugiere que el proveedor no debe permitir que los usuarios cambien las propiedades de configuración. Esta marca solo es una sugerencia; se puede pasar por alto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La hoja de propiedades de configuración se mostró correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El objeto status no admite este método, tal y como indica la ausencia de la marca STATUS_SETTINGS_DIALOG en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIStatus:: SettingsDialog** muestra una hoja de propiedades de configuración. Todos los proveedores de servicios deben admitir el método **SettingsDialog** , pero no es necesario. Los proveedores de servicios pueden implementar sus propias hojas de propiedades o usar la implementación suministrada en el método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) del objeto support. **DoConfigPropsheet** genera una hoja de propiedades de lectura y escritura. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si un proveedor de transporte remoto tiene alguna configuración, debe hacer lo siguiente:
  
- Abra la sección de perfil del proveedor de transporte.
    
- Obtiene la configuración de la propiedad del proveedor de transporte del perfil.
    
- Mostrar la configuración de la propiedad en un cuadro de diálogo.
    
- Si el cuadro de diálogo permite editar la configuración de la propiedad, compruebe que la nueva configuración es válida y vuelva a almacenarla en la sección de perfil del proveedor de transporte.
    
- Devuelve S_OK o todos los valores de error devueltos durante los pasos anteriores.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la hoja de propiedades que se muestra a través de **SettingsDialog** para realizar una serie de tareas, como las siguientes: 
  
- Especifique un almacén de mensajes predeterminado.
    
- Especifique un orden de transporte.
    
- Especifique un contenedor de libreta de direcciones predeterminado para la exploración.
    
- Especifique un orden de búsqueda para resolver nombres ambiguos.
    
- Especifique una libreta personal de direcciones predeterminada.
    
Los proveedores de servicios pueden implementar las hojas de propiedades que son de lectura y escritura, de solo lectura o de combinación de permisos, según la propiedad. Los proveedores de servicios pueden implementar diferentes permisos en propiedades individuales mediante la configuración de restricciones de propiedad. El modo predeterminado de las hojas de propiedades es de lectura y escritura. Puede solicitar hojas de propiedades de solo lectura estableciendo la marca UI_READONLY en las llamadas a **SettingsDialog**. Los proveedores de servicios que son capaces de implementar hojas de propiedades de solo lectura pueden hacerlo. Sin embargo, dado que algunos proveedores de servicios no pueden reemplazar el modo predeterminado, debe estar preparado para controlar las hojas de propiedades de ambos tipos. 
  
Como una interfaz de usuario siempre está involucrada en esta operación, solo los clientes interactivos deben llamar a **SettingsDialog**.
  
## <a name="see-also"></a>Ver también



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

