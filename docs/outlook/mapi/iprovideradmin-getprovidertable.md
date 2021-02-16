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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434476"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de proveedores del servicio de mensajes, una lista de los proveedores de servicios en el servicio de mensajes.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas en las columnas de la tabla del proveedor. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no MAPI_UNICODE marca, las columnas tienen el formato ANSI.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla del proveedor se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IProviderAdmin::GetProviderTable** recupera un puntero a la tabla de proveedor del servicio de mensajes, una tabla que MAPI mantiene y que contiene información sobre cada proveedor de servicios en el servicio de mensajes. 
  
A diferencia de la tabla de proveedor devuelta por el método [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) la tabla de proveedor devuelta por **IProviderAdmin::GetProviderTable** puede incluir filas adicionales que representan información asociada a uno o varios de los proveedores de servicios en el servicio de mensajes. Esta información adicional se agrega al perfil con la palabra clave "Sections" del archivo Mapisvc.inf. Cuando un proveedor tiene secciones de perfil adicionales, almacena las estructuras **MAPIUID** para estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** se guarda en la sección perfil del servicio de mensajes. 
  
Los proveedores que se han eliminado o que están en uso pero que se han marcado para su eliminación no se incluyen en la tabla del proveedor. Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del servicio de mensajes no se reflejan en la tabla. 
  
Si el servicio de mensajes no tiene proveedores, **IProviderAdmin::GetProviderTable** devuelve una tabla con cero filas y S_OK valor devuelto. 
  
Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
Para obtener una lista completa de las columnas de la tabla del proveedor, vea [Tabla de proveedores](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar las filas de una tabla de proveedor en orden de transporte, ordene la tabla por la **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Para recuperar solo las filas que representan proveedores de servicios (sin incluir filas adicionales), limite la recuperación a las filas que tienen un valor de PT_ERROR en su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa el **método IProviderAdmin::GetProviderTable** para obtener la tabla de proveedores que se representará en un cuadro de diálogo nuevo.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

