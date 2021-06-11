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
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427202"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece criterios de búsqueda para el contenedor.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> [in] Puntero a una [estructura SRestriction](srestriction.md) que define los criterios de búsqueda. Si se pasa NULL en el parámetro  _lpRestriction,_ se volverán a usar los criterios de búsqueda que se usaron más recientemente para este contenedor. Null no debe pasarse en  _lpRestriction para_ la primera búsqueda en un contenedor. 
    
 _lpContainerList_
  
> [in] Puntero a una matriz de identificadores de entrada que representan contenedores que se incluirán en la búsqueda. Si un cliente pasa NULL en el parámetro  _lpContainerList,_ los identificadores de entrada usados más recientemente para buscar en este contenedor se usan para la nueva búsqueda. Un cliente no debe pasar NULL en  _lpContainerList_ para la primera búsqueda en un contenedor. 
    
 _ulSearchFlags_
  
> [in] Máscara de bits de marcas que controlan cómo se realiza la búsqueda. Se pueden establecer las siguientes marcas:
    
BACKGROUND_SEARCH 
  
> La búsqueda debe ejecutarse con prioridad normal con respecto a otras búsquedas. Esta marca no se puede establecer al mismo tiempo que la FOREGROUND_SEARCH marca.
    
FOREGROUND_SEARCH 
  
> La búsqueda debe ejecutarse con prioridad alta con respecto a otras búsquedas. Esta marca no se puede establecer al mismo tiempo que la BACKGROUND_SEARCH marca.
    
NON_CONTENT_INDEXED_SEARCH
  
> La búsqueda no debe usar la indización de contenido para buscar entradas que coincidan. Esta marca solo es válida para Exchange almacenes.
    
RECURSIVE_SEARCH 
  
> La búsqueda debe incluir los contenedores especificados en el  _parámetro lpContainerList_ y todos sus contenedores secundarios. Esta marca no se puede establecer al mismo tiempo que la SHALLOW_SEARCH marca. 
    
RESTART_SEARCH 
  
> La búsqueda debe iniciarse si se trata de la primera llamada a **SetSearchCriteria** o reiniciarse si la búsqueda está inactiva. Esta marca no se puede establecer al mismo tiempo que la marca STOP_SEARCH marca.
    
SHALLOW_SEARCH 
  
> La búsqueda solo debe buscarse en los contenedores especificados en el parámetro  _lpContainerList_ para las entradas que coincidan. Esta marca no se puede establecer al mismo tiempo que la marca RECURSIVE_SEARCH marca. 
    
STOP_SEARCH 
  
> La búsqueda debe detenerse. Esta marca no se puede establecer al mismo tiempo que la RESTART_SEARCH marca.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los criterios de búsqueda se han establecido correctamente.
    
MAPI_E_TOO_COMPLEX 
  
> El proveedor de servicios no admite los criterios de búsqueda especificados.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIContainer::SetSearchCriteria** establece criterios de búsqueda para un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda. Una carpeta de resultados de búsqueda contiene vínculos a los mensajes que cumplen los criterios de búsqueda; los mensajes reales se siguen almacenando en sus ubicaciones originales. Los únicos datos únicos que se incluyen en una carpeta de resultados de búsqueda es su tabla de contenido. La tabla de contenido de una carpeta de resultados de búsqueda tiene el contenido combinado del almacén de mensajes después de aplicar la restricción de búsqueda. 
  
Una operación de búsqueda solo funciona en esta tabla de contenido combinado; no busca en otras carpetas de resultados de búsqueda. Los resultados de la búsqueda devuelven solo los mensajes que coinciden con los criterios de búsqueda; no se devuelve la jerarquía de carpetas.
  
El control se devuelve al cliente cuando finaliza la búsqueda.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los contenedores de libreta de direcciones establecen criterios de búsqueda aplicando restricciones a sus tablas de contenido. Para obtener más información acerca de los criterios de búsqueda y los contenedores de libreta de direcciones, vea [Implementing Advanced Searching](implementing-advanced-searching.md).
  
Debe admitir operaciones abiertas, copiar, mover y eliminar en los mensajes de las carpetas de resultados de búsqueda, no en la propia carpeta de resultados de búsqueda. No permita que los mensajes se creen en una carpeta de resultados de búsqueda ni se copien en una carpeta. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para buscar destinatarios de mensajes, establezca  _lpRestriction_ para que apunte a una restricción de subobjeto con el **miembro ulSubObject** de la estructura [SSubRestriction](ssubrestriction.md) establecida en **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Para buscar datos adjuntos, establezca el **miembro ulSubObject** **en PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Establezca el **miembro lpRes** para que señale a una restricción de propiedad que describa los criterios de búsqueda de los destinatarios o datos adjuntos. 
  
Por ejemplo, para buscar datos adjuntos de archivo que tengan la extensión .mss, establezca **ulSubObject** en **PR_MESSAGE_ATTACHMENTS** y **lpRes** en una restricción de propiedad que coincida **con PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) con .mss.
  
Establecer la FOREGROUND_SEARCH en el  _parámetro ulSearchFlags_ podría provocar una disminución en el rendimiento del sistema. 
  
Puede usar **SetSearchCriteria para** cambiar los criterios de búsqueda de una búsqueda que ya está en curso. Puede especificar nuevas restricciones, nuevas listas de carpetas para buscar y una nueva prioridad de búsqueda, como actualizar una búsqueda a una prioridad más alta. Los cambios en la prioridad de búsqueda no hacen que se reinicie una búsqueda existente, pero pueden producirse otros cambios en los criterios de búsqueda. 
  
Cuando esté usando una carpeta de resultados de búsqueda, puede eliminar la carpeta o dejarla abierta para su uso posterior. Si elimina la carpeta de resultados de búsqueda, solo se eliminarán los vínculos de mensaje. Los mensajes reales permanecen en sus carpetas primarias. 
  
Para obtener más información acerca de las carpetas de resultados de búsqueda, vea [Carpetas de búsqueda MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa el **método IMAPIContainer::SetSearchCriteria** para escribir criterios de búsqueda para una carpeta después de que un usuario la haya editado.  <br/> |
   
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

