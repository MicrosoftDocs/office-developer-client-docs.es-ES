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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817609"
---
# <a name="imapitablerestrict"></a>IMAPITable:: Restrict

  
  
**Se aplica a**: Outlook 
  
Se aplica un filtro a una tabla, reducción de la fila que se establece en sólo las filas que coincidan con los criterios especificados.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Sintaxis

 _lpRestriction_
  
> [entrada] Puntero a una estructura de [SRestriction](srestriction.md) definición de las condiciones del filtro. Pasar NULL en el parámetro _lpRestriction_ , quita el filtro actual. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla la sincronización de la operación de restricción. Se pueden establecer los siguientes indicadores:
    
TBL_ASYNC 
  
> Inicia la operación de forma asincrónica y devuelve antes de que finalice la operación.
    
TBL_BATCH 
  
> Difiere la evaluación del filtro hasta que los datos de la tabla están necesarios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El filtro se ha aplicado correctamente.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de restricción de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_TOO_COMPLEX 
  
> La tabla no puede realizar la operación porque el filtro determinado indicado por el parámetro _lpRestriction_ es demasiado complicado. 
    
## <a name="remarks"></a>Notas

El método **IMAPITable:: Restrict** establece una restricción, o un filtro, en una tabla. Si hay una restricción anterior, se descarta y aplica uno nuevo. Aplicar una restricción no tiene ningún efecto en los datos subyacentes de una tabla; simplemente se modifica la vista al limitar las filas que se pueden recuperar a las filas que contienen datos que cumplen la restricción. 
  
Hay varios tipos diferentes de las restricciones, cada uno de ellos se describe con una estructura diferente. La estructura de [SRestriction](srestriction.md) contiene dos miembros: un valor que indica el tipo de restricción y la estructura específica aplicable para ese tipo. 
  
Las notificaciones para las filas de tabla que están ocultos de la vista mediante llamadas a **Restrict** nunca se generan. 
  
Una restricción de propiedad en una propiedad multivalor funciona como una restricción en una propiedad de un solo valor. Una propiedad multivalor para usarse en una restricción de propiedad debe tener la marca MVI_FLAG establecida. Si no tiene este indicador establecido, se trata como una tupla totalmente ordenada. Una comparación de dos columnas con varios valores compara los elementos de columna en orden, la relación de las columnas en la primera desigualdad de informes. Igualdad se devuelve sólo si las columnas que se comparan contienen los mismos valores en el mismo orden. Si una columna tiene menos valores que el otro, la relación conocida es un valor nulo en el otro valor.
  
Para obtener más información acerca de las restricciones, vea [Restricciones de sobre](about-restrictions.md).
  
> [!NOTE]
> Si crea consultas dinámicas para buscar datos en el servidor, use el método **FindRow** en lugar de usar el método **Restrict** y el método **QueryRows** juntos. El método **Restrict** crea una vista en caché que se usa para evaluar todos los mensajes, agregar o modificar en la carpeta base. Si una aplicación cliente usa el método **Restrict** para cada consulta dinámica, se creará una vista en caché para cada consulta. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para descartar la restricción actual sin crear una nueva, pase NULL en _lpRestriction_.
  
Si hay otra llamada tabla asincrónica en curso, lo que provoca que **Restrict** devolver MAPI_E_BUSY, puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la llamada. 
  
 **Restrict** funciona de forma sincrónica a menos que establezca uno de los indicadores. Si se establece la marca TBL_BATCH, **Restrict** pospone la evaluación de la restricción a menos que solicitar los datos. Si se establece la marca TBL_ASYNC, **Restrict**funciona de forma asincrónica, potencialmente devolver antes de la finalización de la operación.
  
Cuando se realiza una llamada a **Restrict** y BOOKMARK_CURRENT, la posición actual del cursor, se establece en el principio de la tabla, se descartan todos los marcadores de una tabla. 
  
Si se intenta imponer una restricción de propiedad en una propiedad que no está en el conjunto de columnas de la tabla, los resultados son no definidos. Siempre que no está seguro de si se admite una propiedad en una tabla, combinar la restricción de propiedad con una restricción de existe. El existe restricción comprueba la existencia de la propiedad antes de intentar imponer la restricción de propiedad. 
  
No se debe esperar recibir una notificación de tabla en una fila que se ha filtrado de una tabla debido a una restricción.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI usa el método **IMAPITable:: Restrict** para establecer una restricción en una tabla.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPITable::Abort](imapitable-abort.md)
  
[Elemento IMAPITable:: FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable:: QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

