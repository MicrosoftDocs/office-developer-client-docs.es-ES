---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817921"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Hace referencia a**: Outlook 
  
Proporciona acceso a la tabla de proveedor del servicio de mensajes, una lista de los proveedores de servicios en el servicio de mensajes.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas devueltas en columnas de la tabla proveedor. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las columnas de cadena se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas están en formato ANSI.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de proveedor se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin::GetProviderTable** recupera un puntero a la tabla de proveedor del servicio de mensajes, una tabla que mantiene la MAPI que contiene información acerca de cada proveedor de servicios en el servicio de mensajes. 
  
A diferencia de la tabla de proveedor devuelta por el método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , en la tabla de proveedor devuelta por **IProviderAdmin::GetProviderTable** puede incluir filas adicionales que representan información asociada con una o varias de los proveedores de servicios en el servicio de mensajes. Esta información adicional se agrega al perfil con la palabra clave "Secciones" del archivo Mapisvc.inf. Cuando un proveedor tiene secciones de perfil adicional, almacena las estructuras **MAPIUID** para estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** se guarda en la sección de perfil de servicio de mensaje. 
  
Los proveedores que se han eliminado, o están en uso, se han marcado para su eliminación, pero no se incluyen en la tabla proveedor. Tablas de proveedor son estáticas, lo que significa que las adiciones posteriores a o eliminaciones desde el servicio de mensajes no se reflejan en la tabla. 
  
Si el servicio de mensajes no tiene ningún proveedor, **IProviderAdmin::GetProviderTable** devuelve un objeto table con cero filas y el valor devuelto de S_OK. 
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
Para obtener una lista completa de las columnas en la tabla de proveedor, vea la [Tabla de proveedor](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar las filas de una tabla de proveedor en el orden de transporte, ordenar la tabla por la columna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Para recuperar sólo las filas que representan los proveedores de servicios (sin incluir filas adicionales), limitar la recuperación a las filas que tienen un valor de PT_ERROR en su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa el método **IProviderAdmin::GetProviderTable** para obtener la tabla de proveedores para representar en un cuadro de diálogo nuevo.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

