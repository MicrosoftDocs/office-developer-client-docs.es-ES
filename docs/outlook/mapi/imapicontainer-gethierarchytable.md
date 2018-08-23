---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563803"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a la tabla de jerarquía del contenedor.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se devuelve información de la tabla. Se pueden establecer los siguientes indicadores:
    
CONVENIENT_DEPTH 
  
> Rellena la tabla de jerarquía con contenedores de varios niveles. Si no se establece CONVENIENT_DEPTH, en la tabla de jerarquía contiene sólo los contenedores de secundarios inmediatos del contenedor.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** puede devolver correctamente, posiblemente antes de que la tabla está disponible para el autor de la llamada. Si no está disponible en la tabla, realizar una llamada de tabla subsiguiente puede producir un error. 
    
MAPI_UNICODE. 
  
> Solicitudes que se devuelven las columnas que contienen datos de cadena en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., se deben devolver las cadenas en formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que actualmente están marcados como suaves eliminan, es decir, se encuentran en la retención de elementos eliminados fase de tiempo.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de jerarquía.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de jerarquía se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El contenedor tiene los contenedores secundarios y no puede proporcionar una tabla de jerarquía.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer::GetHierarchyTable** devuelve un puntero a la tabla de jerarquía de un contenedor. Una tabla de jerarquía contiene información de resumen acerca de los contenedores secundarios en el contenedor. Tablas de jerarquía de carpeta almacenar información acerca de las subcarpetas; tablas de jerarquía de la libreta de direcciones contienen información acerca de secundarios contenedores de la libreta de direcciones y listas de distribución. 
  
Es posible que algunos contenedores tener ningún contenedores secundarios. Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetHierarchyTable**.
  
Cuando se establece la marca CONVENIENT_DEPTH, cada fila de la tabla de jerarquía incluye también la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como una columna. **PR_DEPTH** indica el nivel de cada contenedor en relación con el contenedor que implementa la tabla. Secundarios inmediatos del contenedor de implementación son contenedores en profundidad de cero, los contenedores secundarios de los contenedores de profundidad cero se encuentran en profundidad de uno y así sucesivamente. Los valores de **PR_DEPTH** aumentan secuencialmente como profundiza la jerarquía de niveles. 
  
Para obtener una lista completa de columnas opcionales y obligatorios en las tablas de jerarquía, vea [Las tablas de jerarquía](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si decide admitir una tabla de jerarquías de su contenedor, también debe hacer lo siguiente:
  
- Admite una llamada al método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Devolver **PR_CONTAINER_HIERARCHY** de una llamada a los métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md) o [IMAPIProp::GetProps](imapiprop-getprops.md) del contenedor. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las columnas de tabla de contenido de cadena y binaria se pueden truncar. Normalmente, los proveedores devuelven 255 caracteres. Debido a que no se conoce de antemano si una tabla incluye columnas truncadas, supongamos que una columna se trunca si la longitud de la columna es de 255 o 510 bytes. Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirlo y, a continuación, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Dependiendo del proveedor en la implementación, las restricciones y las operaciones de ordenación pueden aplicar a toda la cadena o a la versión truncada de dicha cadena. Además, no se garantiza que los proveedores de almacén para respetar el conjunto de criterio de ordenación [que ssortorderset](ssortorderset.md) especificado para tablas de jerarquía. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |La clase CHierarchyTableTreeCtrl utiliza **GetHierarchyTable** para obtener las tablas de jerarquía para mostrar en un control de vista de árbol.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

