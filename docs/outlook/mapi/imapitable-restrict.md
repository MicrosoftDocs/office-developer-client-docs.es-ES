---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414623"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aplica un filtro a una tabla, lo que reduce el conjunto de filas a solo aquellas filas que coincidan con los criterios especificados.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> [in] Puntero a una [estructura SRestriction](srestriction.md) que define las condiciones del filtro. Si se pasa NULL en el  _parámetro lpRestriction,_ se quita el filtro actual. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tiempo de la operación de restricción. Se pueden establecer las siguientes marcas:
    
TBL_ASYNC 
  
> Inicia la operación de forma asincrónica y devuelve antes de que finalice la operación.
    
TBL_BATCH 
  
> Aplaza la evaluación del filtro hasta que se requieran los datos de la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El filtro se aplicó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de restricción. Debe permitirse completar la operación en curso o detenerse.
    
MAPI_E_TOO_COMPLEX 
  
> La tabla no puede realizar la operación porque el filtro determinado al que apunta el parámetro  _lpRestriction_ es demasiado complicado. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::Restrict** establece una restricción o filtro en una tabla. Si hay una restricción anterior, se descarta y se aplica la nueva. Aplicar una restricción no afecta a los datos subyacentes de una tabla; simplemente modifica la vista limitando las filas que se pueden recuperar a filas que contienen datos que satisfacen la restricción. 
  
Hay varios tipos diferentes de restricciones, cada una descrita con una estructura diferente. La [estructura SRestriction](srestriction.md) contiene dos miembros: un valor que indica el tipo de restricción y la estructura específica aplicable a ese tipo. 
  
Las notificaciones de las filas de tabla ocultas de la vista por llamadas a **Restrict** nunca se generan. 
  
Una restricción de propiedad en una propiedad multivalor funciona como una restricción en una propiedad de un solo valor. Una propiedad multivalor que se va a usar en una restricción de propiedad debe tener el MVI_FLAG de marca. Si no tiene esta marca establecida, se trata como una tupla totalmente ordenada. Una comparación de dos columnas multivalor compara los elementos de columna en orden, informando de la relación de las columnas en la primera desigualdad. La igualdad solo se devuelve si las columnas comparadas contienen los mismos valores en el mismo orden. Si una columna tiene menos valores que la otra, la relación notificada es la de un valor nulo con el otro valor.
  
Para obtener más información acerca de las restricciones, vea [Acerca de las restricciones](about-restrictions.md).
  
> [!NOTE]
> Si crea consultas dinámicas para buscar datos en el servidor, use el método **FindRow** en lugar de usar el método **Restrict** y el **método QueryRows** juntos. El **método Restrict** crea una vista en caché que se usa para evaluar todos los mensajes agregados o modificados en la carpeta base. Si una aplicación cliente usa el **método Restrict** para cada consulta dinámica, se creará una vista en caché para cada consulta. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para descartar la restricción actual sin crear una nueva, pase NULL en  _lpRestriction_.
  
Si hay otra llamada de tabla asincrónica en curso, lo que hace que **Restrict** devuelva MAPI_E_BUSY, puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la llamada. 
  
 **Restrict** funciona de forma sincrónica a menos que establezca una de las marcas. Si establece la marca TBL_BATCH, **Restrict** pospone la evaluación de la restricción a menos que solicite los datos. Si se TBL_ASYNC marca, **Restrict** funciona de forma asincrónica, lo que podría devolverse antes de finalizar la operación.
  
Todos los marcadores de una tabla se descartan cuando se realiza una llamada a **Restrict** y BOOKMARK_CURRENT, la posición actual del cursor, se establece en el principio de la tabla. 
  
Si intenta imponer una restricción de propiedad a una propiedad que no está en el conjunto de columnas de la tabla, los resultados no están definidos. Siempre que no esté seguro de si se admite una propiedad en una tabla, combine la restricción de propiedad con una restricción existente. La restricción existe comprueba la existencia de la propiedad antes de intentar imponer la restricción de propiedad. 
  
No espere recibir una notificación de tabla en una fila que se haya filtrado de una tabla debido a una restricción.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI usa el **método IMAPITable::Restrict** para establecer una restricción en una tabla.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

