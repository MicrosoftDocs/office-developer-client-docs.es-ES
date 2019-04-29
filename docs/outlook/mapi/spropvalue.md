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
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **ulPropTag**
  
> Etiqueta de propiedad de la propiedad. Las etiquetas de propiedad son enteros sin signo de 32 bits que constan del identificador único de la propiedad en los 16 bits de orden superior y el tipo de la propiedad en los 16 bits de orden inferior.
    
 **dwAlignPad**
  
> Reservado para MAPI; No use. 
    
 **Valor**
  
> Unión de valores de datos, el valor específico que dicta el tipo de propiedad. En la tabla siguiente se enumeran para cada tipo de propiedad, el miembro de la Unión que se debe usar y su tipo de datos asociado.
    
|**Tipo de propiedad**|**Valor**|**Tipo de datos de valor**|
|:-----|:-----|:-----|
|PT_I2 o PT_SHORT  <br/> |**k** <br/> |short int  <br/> |
|PT_I4 o PT_LONG (con signo)  <br/> |**l** <br/> |DESDE  <br/> |
|PT_I4 o PT_LONG (sin asignar)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 o PT_FLOAT  <br/> |**FLT** <br/> |float  <br/> |
|PT_R8 o PT_DOUBLE  <br/> |**japonesa** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**n** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**Espacia** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**Veamos** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**cm** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**definido** <br/> |BYTE [matriz]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 o PT_LONGLONG  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
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
|PT_NULL o PT Object  <br/> |**x** <br/> |DESDE  <br/> |
|PT_PTR  <br/> |**LPV** <br/> |EFECTO\*  <br/> |
   
## <a name="remarks"></a>Comentarios

El miembro **ulPropTag** está formado por dos partes: 
  
- Un identificador en los 16 bits de orden superior.
    
- Un tipo en los 16 bits de orden inferior.
    
El identificador es un valor numérico dentro de un intervalo determinado. MAPI define los intervalos de los identificadores para describir para qué se usa la propiedad y quién es responsable de su mantenimiento. MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags. h.
  
El tipo indica el formato del valor de la propiedad. MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs. h. 
  
Para obtener una lista completa de los intervalos de propiedades válidos para los identificadores y tipos de propiedades, vea el apéndice [identificadores y tipos de propiedades](property-identifiers-and-types.md) . 
  
El miembro **dwAlignPad** se usa como relleno para garantizar una alineación adecuada en los equipos que requieren una alineación de 8 bytes para los valores de 8 bytes. Los desarrolladores que escriben código en estos equipos deben usar rutinas de asignación de memoria que asignan las matrices de **SPropValue** en límites de 8 bytes. 
  
Para obtener más información, consulte [información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [actualizar las propiedades MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Ver también



[Estructuras MAPI](mapi-structures.md)

