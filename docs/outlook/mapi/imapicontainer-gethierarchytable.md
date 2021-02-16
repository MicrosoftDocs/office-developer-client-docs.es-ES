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
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426201"
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

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se devuelve la información en la tabla. Se pueden establecer las siguientes marcas:
    
CONVENIENT_DEPTH 
  
> Rellena la tabla de jerarquía con contenedores de varios niveles. Si CONVENIENT_DEPTH no se establece, la tabla de jerarquía contiene solo los contenedores secundarios inmediatos del contenedor.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** puede devolverse correctamente, posiblemente antes de que la tabla esté disponible para el autor de la llamada. Si la tabla no está disponible, realizar una llamada de tabla posterior puede generar un error. 
    
MAPI_UNICODE 
  
> Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode. Si no MAPI_UNICODE marca, las cadenas deben devolverse en formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, están en la fase de tiempo de retención de elementos eliminados.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de jerarquía.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de jerarquía se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El contenedor no tiene contenedores secundarios y no puede proporcionar una tabla de jerarquía.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIContainer::GetHierarchyTable** devuelve un puntero a la tabla de jerarquía de un contenedor. Una tabla de jerarquía contiene información de resumen sobre los contenedores secundarios del contenedor. Las tablas de jerarquía de carpetas tienen información sobre subcarpetas; Las tablas de jerarquía de libretas de direcciones incluyen información sobre los contenedores de libretas de direcciones secundarios y las listas de distribución. 
  
Es posible que algunos contenedores no tengan contenedores secundarios. Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones **de GetHierarchyTable**.
  
Cuando se CONVENIENT_DEPTH marca, cada fila de la tabla de jerarquía también incluye la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como una columna. **PR_DEPTH** indica el nivel de cada contenedor en relación con el contenedor que implementa la tabla. Los contenedores secundarios inmediatos del contenedor de implementación están en profundidad cero, los contenedores secundarios en los contenedores de profundidad cero están en profundidad uno, y así sucesivamente. Los valores de **PR_DEPTH** aumentan secuencialmente a medida que aumenta la jerarquía de niveles. 
  
Para obtener una lista completa de las columnas obligatorias y opcionales de las tablas de jerarquía, vea [Tablas de jerarquía.](hierarchy-tables.md)
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si admite una tabla de jerarquía para el contenedor, también debe hacer lo siguiente:
  
- Admite una llamada al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Devuelve **PR_CONTAINER_HIERARCHY** de una llamada a los métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md) o [IMAPIProp::GetProps del](imapiprop-getprops.md) contenedor. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las columnas de tabla de contenido binario y de cadena se pueden truncar. Normalmente, los proveedores devuelven 255 caracteres. Como no puede saber de antemano si una tabla incluye columnas truncadas, suponga que una columna se trunca si la longitud de la columna es de 255 o 510 bytes. Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto usando su identificador de entrada para abrirlo y, a continuación, llamando al método [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda la cadena o a la versión truncada de esa cadena. Además, no se garantiza que los proveedores de almacén respetarán el conjunto de criterios de ordenación [especificado](ssortorderset.md) para las tablas de jerarquía. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |La clase CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obtener tablas de jerarquía para mostrar en un control de vista de árbol.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

