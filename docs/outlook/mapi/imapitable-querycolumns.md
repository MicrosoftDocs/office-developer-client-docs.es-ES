---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410108"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una lista de columnas para la tabla.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que indica qué conjunto de columnas se debe devolver. Se puede establecer la siguiente marca:
    
TBL_ALL_COLUMNS 
  
> La tabla debe devolver todas las columnas disponibles.
    
 _lpPropTagArray_
  
> [salida] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad del conjunto de columnas. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El conjunto de columnas se devolvió correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de recuperación del conjunto de columnas. La operación en curso debe poder completarse o debe detenerse.
    
## <a name="remarks"></a>Comentarios

Se **puede llamar al método IMAPITable::QueryColumns** para recuperar: 
  
- Conjunto de columnas predeterminado para una tabla.
    
- La columna actual establecida para una tabla, como se establece mediante una llamada al método [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- El conjunto de columnas completo de una tabla, las columnas que están disponibles, pero no necesariamente parte del conjunto actual.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Si no establece la marca TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** devuelve el conjunto de columnas actual o predeterminado de una tabla, dependiendo de si la tabla se ha visto afectada por una llamada a **IMAPITable::SetColumns**. **SetColumns cambia** el orden y la selección de columnas en el conjunto de columnas de una tabla. 
  
Si establece la marca TBL_ALL_COLUMNS, **QueryColumns** devuelve todas las columnas que pueden estar en el conjunto de columnas de la tabla. 
  
Libera la memoria de la matriz de etiquetas de propiedades a la que apunta el parámetro _lpPropTagArray_ llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI usa el **método IMAPITable::QueryColumns** para recuperar el conjunto de columnas actual de una tabla para que el usuario pueda editarla.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

