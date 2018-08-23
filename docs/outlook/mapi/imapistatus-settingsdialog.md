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
ms.openlocfilehash: a21feb474ef69da9ec8e36e06c8649b9d0f93981
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566708"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra una hoja de propiedades que permite al usuario que cambie la configuración de un proveedor de servicios que este método no se admite en los objetos de estado que implementa MAPI.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de la hoja de propiedades de configuración.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la presentación de la hoja de propiedades. Se puede establecer la marca siguiente:
    
UI_READONLY 
  
> Sugiere que el proveedor no debe habilitar a los usuarios cambiar las propiedades de configuración. Esta marca es sólo una sugerencia; se puede hacer caso omiso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La hoja de propiedades de configuración se mostró correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El objeto de estado no es compatible con este método, como se indica por la ausencia de la marca STATUS_SETTINGS_DIALOG en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Comentarios

El método **SettingsDialog** muestra una hoja de propiedades de configuración. Todos los proveedores de servicios deben admitir el método de **diálogo Configuración** , pero no es necesario. Proveedores de servicio pueden implementar sus propias hojas (propiedad) o utilizar la implementación proporcionada en el soporte técnico método del objeto [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) . **DoConfigPropsheet** crea una hoja de propiedades de lectura y escritura. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si un proveedor de transporte remoto tiene cualquier opción de configuración, debe hacer lo siguiente:
  
- Abrir la sección de perfil del proveedor de transporte.
    
- Obtenga el transporte valores de la propiedad del proveedor del perfil.
    
- Mostrar los valores de propiedad en un cuadro de diálogo.
    
- Si el cuadro de diálogo permite la edición de la configuración de propiedades, compruebe que la nueva configuración es válida y almacenarlas atrás en la sección de perfil del proveedor de transporte.
    
- Devolver S_OK o los valores de error devueltos durante los pasos anteriores.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la hoja de propiedades que se muestra a través de **diálogo Configuración** para realizar diversas tareas, como las siguientes: 
  
- Especificar un almacén de mensajes predeterminado.
    
- Especificar un orden de transporte.
    
- Especificar un contenedor de libreta de direcciones predeterminada para la exploración.
    
- Especificar un criterio de búsqueda para resolver nombres ambiguos.
    
- Especifique una libreta de direcciones personales de forma predeterminada.
    
Pueden implementar proveedores de servicios de las hojas de propiedades que son de lectura y escritura, de sólo lectura, o una combinación de permisos, dependiendo de la propiedad. Proveedores de servicios pueden implementar permisos diferentes en las propiedades individuales mediante la configuración de restricciones de propiedad. El modo predeterminado para las hojas de propiedades es de lectura y escritura. Puede solicitar las hojas de propiedades de sólo lectura estableciendo el indicador UI_READONLY en las llamadas al **diálogo Configuración**. Proveedores de servicios que se pueden implementar las hojas de propiedades de sólo lectura pueden hacerlo. Sin embargo, debido a que algunos proveedores de servicios no pueden reemplazar el modo predeterminado, debe estar preparado para tratar las hojas de propiedades de cualquier tipo. 
  
Debido a que una interfaz de usuario siempre está relacionada con esta operación, sólo los clientes interactivos deben llamar **diálogo Configuración**.
  
## <a name="see-also"></a>Recursos adicionales



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

