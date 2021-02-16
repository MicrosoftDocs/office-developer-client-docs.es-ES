---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433531"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una propiedad MAPI.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Miembros

 **ulPropTag**
  
> Etiqueta de propiedad de la propiedad. Las etiquetas de propiedad son enteros sin signo de 32 bits formados por el identificador único de la propiedad en el orden alto de 16 bits y el tipo de la propiedad en orden bajo de 16 bits.
    
 **dwAlignPad**
  
> Reservado para MAPI; no usar. 
    
 **Valor**
  
> Unión de valores de datos, el valor específico determinado por el tipo de propiedad. En la tabla siguiente se enumeran cada tipo de propiedad, el miembro de la unión que se debe usar y su tipo de datos asociado.
    
|**Tipo de propiedad**|**Valor**|**Tipo de datos del valor**|
|:-----|:-----|:-----|
|PT_I2 o PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 o PT_LONG (firmado)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 o PT_LONG (sin signo)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 o PT_FLOAT  <br/> |**flt** <br/> |float  <br/> |
|PT_R8 o PT_DOUBLE  <br/> |**dbl** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**at** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [matriz]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 o PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL o PT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID \*  <br/> |
   
## <a name="remarks"></a>Comentarios

El **miembro ulPropTag** se conste de dos partes: 
  
- Un identificador de 16 bits de orden alto.
    
- Un tipo en orden bajo de 16 bits.
    
El identificador es un valor numérico dentro de un intervalo determinado. MAPI define intervalos para que los identificadores describan para qué se usa la propiedad y quién es responsable de su mantenimiento. MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.
  
El tipo indica el formato del valor de la propiedad. MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h. 
  
Para obtener una lista completa de los intervalos de propiedades válidos para identificadores y tipos de propiedad, vea el apéndice Identificadores y [tipos de](property-identifiers-and-types.md) propiedad. 
  
El **miembro dwAlignPad** se usa como espaciado interno para garantizar la alineación correcta en equipos que requieren alineación de 8 bytes para valores de 8 bytes. Los desarrolladores que escriben código en estos equipos deben usar rutinas de asignación de memoria que asignen las matrices **SPropValue** en límites de 8 bytes. 
  
Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y actualización de propiedades [MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Consulte también



[Estructuras MAPI](mapi-structures.md)

