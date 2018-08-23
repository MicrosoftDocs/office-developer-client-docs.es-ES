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
ms.openlocfilehash: 60528162917a8a383060adbcadefb610aa42ce32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580974"
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

## <a name="members"></a>Members

 **ulPropTag**
  
> Etiqueta de la propiedad para la propiedad. Las etiquetas de propiedad son enteros sin signo de 32 bits que consta del identificador único de la propiedad de orden superior a 16 bits y el tipo de propiedad de orden inferior a 16 bits.
    
 **dwAlignPad**
  
> Reservado para MAPI; No use. 
    
 **Valor**
  
> Unión de los valores de datos, el valor específico determinado por el tipo de propiedad. En la siguiente tabla se enumera para cada tipo de propiedad, el miembro de la unión que se debe usar y su tipo de datos asociado.
    
|**Tipo de propiedad**|**Valor**|**Tipo de datos del valor**|
|:-----|:-----|:-----|
|PT_I2 o PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 o PT_LONG (firmado)  <br/> |**l** <br/> |LARGO  <br/> |
|PT_I4 o PT_LONG (sin firmar)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 o PT_FLOAT  <br/> |**flt** <br/> |float  <br/> |
|PT_R8 o PT_DOUBLE  <br/> |**doble** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |int corto sin firmar  <br/> |
|PT_CURRENCY  <br/> |**actual** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**en** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**FT** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**Papelera de** <br/> |BYTE [matriz]  <br/> |
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
|PT_NULL o pt Object  <br/> |**x** <br/> |LARGO  <br/> |
|PT_PTR  <br/> |**LPV** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>Comentarios

El miembro **ulPropTag** se compone de dos partes: 
  
- Un identificador de orden superior a 16 bits.
    
- Un tipo de orden inferior a 16 bits.
    
El identificador es un valor numérico dentro de un intervalo determinado. MAPI define los intervalos para los identificadores describir la propiedad que se usa para y quién es responsable de mantenerlo. MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.
  
El tipo indica el formato para el valor de la propiedad. MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h. 
  
Para obtener una lista completa de los intervalos de propiedad válido para los identificadores y tipos de propiedad, consulte el apéndice [identificadores de propiedades y tipos](property-identifiers-and-types.md) . 
  
El miembro **dwAlignPad** se utiliza como relleno para realizar la alineación adecuada seguro en los equipos que requieren la alineación de 8 bytes para los valores de 8 bytes. Los desarrolladores que escribir código en estos equipos deben utilizar rutinas de asignación de memoria que asignan las matrices **SPropValue** en límites de 8 bytes. 
  
Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [Actualizar las propiedades de MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Recursos adicionales



[Estructuras MAPI](mapi-structures.md)

