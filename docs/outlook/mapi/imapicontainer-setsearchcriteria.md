---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817216"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Hace referencia a**: Outlook 
  
Establece los criterios de búsqueda para el contenedor.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpRestriction_
  
> [entrada] Un puntero a una estructura [SRestriction](srestriction.md) que define los criterios de búsqueda. Si se pasa NULL en el parámetro _lpRestriction_ , se usan nuevamente los criterios de búsqueda que se usaron recientemente para este contenedor. No se debe pasar NULL en _lpRestriction_ para la primera búsqueda en un contenedor. 
    
 _lpContainerList_
  
> [entrada] Un puntero a una matriz de identificadores de entrada que representan los contenedores que se deben incluir en la búsqueda. Si un cliente pasa NULL en el parámetro _lpContainerList_ , los identificadores de entrada utilizados más recientemente para buscar este contenedor se usan para la búsqueda nuevo. Un cliente no debe pasar NULL en _lpContainerList_ para la primera búsqueda en un contenedor. 
    
 _ulSearchFlags_
  
> [entrada] Una máscara de bits de indicadores que controlan cómo se realiza la búsqueda. Se pueden establecer los siguientes indicadores:
    
BACKGROUND_SEARCH 
  
> La búsqueda debe ejecutarse con prioridad normal con respecto a otras búsquedas. No se puede establecer esta marca al mismo tiempo, como la marca FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> La búsqueda debe ejecutarse con prioridad alta con respecto a otras búsquedas. No se puede establecer esta marca al mismo tiempo, como la marca BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> La búsqueda no debe usar la indización de contenido para buscar entradas coincidentes. Esta marca sólo es válida para los almacenes de Exchange.
    
RECURSIVE_SEARCH 
  
> La búsqueda debe incluir los contenedores especificados en el parámetro _lpContainerList_ y todas sus contenedores secundarios. No se puede establecer esta marca al mismo tiempo, como la marca SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> La búsqueda debe ser iniciadas por si se trata de la primera llamada a **es posible SetSearchCriteria**o reiniciar si la búsqueda está inactiva. No se puede establecer esta marca al mismo tiempo, como la marca STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> La búsqueda debe tener un aspecto sólo en los contenedores especificados en el parámetro _lpContainerList_ para que coincidan con las entradas. No se puede establecer esta marca al mismo tiempo, como la marca RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> Se debe detener la búsqueda. No se puede establecer esta marca al mismo tiempo, como la marca RESTART_SEARCH.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los criterios de búsqueda se estableció correctamente.
    
MAPI_E_TOO_COMPLEX 
  
> El proveedor de servicios no es compatible con los criterios de búsqueda especificada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer::SetSearchCriteria** establece los criterios de búsqueda para un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda. Una carpeta de resultados de búsqueda contiene vínculos a los mensajes que cumplen los criterios de búsqueda; el número de mensajes aún se almacena en sus ubicaciones originales. Los datos solo únicos que se encuentra en una carpeta de resultados de búsqueda están su tabla de contenido. En la tabla de contenido de una carpeta de resultados de búsqueda tiene el contenido combinado del almacén de mensajes después de que se ha aplicado la restricción de la búsqueda. 
  
Una operación de búsqueda sólo funciona en esta tabla de contenido combinado; no buscará en otras carpetas de resultados de búsqueda. Los resultados de búsqueda devolución únicamente los mensajes que coinciden con los criterios de búsqueda; no se devuelve la jerarquía de carpetas.
  
Control se devuelve al cliente cuando haya finalizado la búsqueda.
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Contenedores de libretas de direcciones establecer los criterios de búsqueda mediante la aplicación de restricciones a sus tablas de contenido. Para obtener más información acerca de los criterios de búsqueda y contenedores de libretas de direcciones, vea [Implementación avanzada buscar](implementing-advanced-searching.md).
  
Debe admitir open, copiar, mover y eliminar operaciones en los mensajes dentro de carpetas de resultados de búsqueda, no en la propia carpeta de resultados de búsqueda. No permitir que los mensajes que se creen dentro o se copian en una carpeta de resultados de búsqueda. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para buscar los destinatarios del mensaje, establezca _lpRestriction_ para que apunte a una restricción de subobjetos con el miembro **ulSubObject** en la estructura de [SSubRestriction](ssubrestriction.md) establecido en **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Para buscar los datos adjuntos, establezca al miembro **ulSubObject** en **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Establezca el miembro **lpRes** para que apunte a una restricción de propiedad que se describe los criterios de búsqueda para los destinatarios o datos adjuntos. 
  
Por ejemplo, para buscar archivos adjuntos que tienen la extensión .mss, establezca **ulSubObject** en **PR_MESSAGE_ATTACHMENTS** y **lpRes** a una restricción de propiedad que coincida con **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) con. mss.
  
Al establecer el indicador FOREGROUND_SEARCH en el parámetro _ulSearchFlags_ podría provocar una disminución del rendimiento del sistema. 
  
**Es posible SetSearchCriteria** se puede usar para cambiar los criterios de búsqueda de una búsqueda ya está en curso. Puede especificar restricciones de nuevo, nuevas listas de carpetas para buscar y una prioridad de búsqueda nueva, como la actualización de una búsqueda con una prioridad superior. Cambios en la prioridad de búsqueda no hacen una búsqueda existente reiniciar, pero pueden otros cambios en los criterios de búsqueda. 
  
Cuando haya terminado el uso de una carpeta de resultados de búsqueda, puede eliminar la carpeta o dejar que permanecen abiertos para su uso posterior. Si se elimina la carpeta de resultados de búsqueda, se eliminan sólo los vínculos de mensaje. Los mensajes reales permanecen en sus carpetas principales. 
  
Para obtener más información acerca de las carpetas de resultados de búsqueda, vea [Las carpetas de búsqueda de MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa el método **IMAPIContainer::SetSearchCriteria** para escribir criterios de búsqueda para una carpeta una vez que un usuario lo ha editado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

