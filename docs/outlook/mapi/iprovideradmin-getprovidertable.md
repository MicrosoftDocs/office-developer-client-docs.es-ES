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
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279531"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de proveedores del servicio de mensajes, una lista de los proveedores de servicios del servicio de mensajes.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas en las columnas de la tabla del proveedor. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las columnas están en formato ANSI.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de proveedores se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin:: GetProviderTable** recupera un puntero a la tabla de proveedores del servicio de mensajes, una tabla que mantiene MAPI que contiene información acerca de cada proveedor de servicios en el servicio de mensajes. 
  
A diferencia de la tabla Provider devuelta por el método [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) , la tabla de proveedores devuelta por **IProviderAdmin:: GetProviderTable** puede incluir filas adicionales que representan la información asociada con uno o varios de los proveedores de servicios del servicio de mensajes. Esta información adicional se agrega al perfil con la palabra clave "Sections" (secciones) del archivo MAPISVC. inf. Cuando un proveedor tiene secciones de perfil adicionales, almacena las estructuras **MAPIUID** para estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** se guarda en la sección Perfil del servicio de mensajes. 
  
Los proveedores que se han eliminado o están en uso pero están marcados para su eliminación no se incluyen en la tabla de proveedores. Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del servicio de mensajes no se reflejan en la tabla. 
  
Si el servicio de mensajes no tiene proveedores, **IProviderAdmin:: GetProviderTable** devuelve una tabla con cero filas y el valor devuelto S_OK. 
  
La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
Para obtener una lista completa de las columnas de la tabla de proveedores, consulte [TABLE Provider](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar las filas de una tabla de proveedores en orden de transporte, ordene la tabla mediante la columna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Para recuperar sólo las filas que representan proveedores de servicios (sin incluir ninguna fila adicional), limite la recuperación a las filas que tienen un valor de PT_ERROR en su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
| MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnDisplayItem  <br/> |MFCMAPI usa el método **IProviderAdmin:: GetProviderTable** para obtener la tabla de proveedores que se representará en un cuadro de diálogo nuevo.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

