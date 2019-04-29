---
title: Tipos de propiedades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 43b0090192a2f9b02acee4edf471c5ae6c6de7e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407056"
---
# <a name="property-types"></a>Tipos de propiedades

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI admite tanto propiedades de valor único como de varios valores. Con una propiedad de un solo valor, hay un valor del tipo base para la propiedad. Con una propiedad de varios valores, hay varios valores del tipo base. 
  
En la tabla siguiente se describen los tipos de propiedades de valor único y de varios valores compatibles con MAPI. Para cada tipo de valor único que tiene un tipo de valor múltiple correspondiente, el tipo de varios valores aparece entre paréntesis después del tipo de valor único.
  
|**Tipo de propiedad**|**Valor hexadecimal**|**Descripción**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |1,0000  <br/> |Indica que el tipo de propiedad es desconocido. Este tipo de propiedad está reservado para su uso con los métodos de interfaz.  <br/> |
|PT_NULL  <br/> |0,001  <br/> |Indica que no hay ningún valor de propiedad. Este tipo de propiedad se reserva para su uso con métodos de interfaz y es el mismo que el tipo OLE VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Entero de 16 bits (2 bytes) con signo. Este tipo de propiedad es el mismo que PT_SHORT (PT_MV_SHORT) y el tipo de OLE VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Entero de 32 bits (4 bytes) firmado o sin firmar. Este tipo de propiedad es el mismo que PT_LONG (PT_MV_LONG) y el tipo de OLE VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |valor de punto flotante de 32 bits (8 bytes). Este tipo de propiedad es el mismo que PT_R4 (PT_MV_R4) y el tipo de OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |valor de punto flotante de 64 bits (8 bytes). Este tipo de propiedad es el mismo que PT_R8 y los tipos OLE VT_R8 y VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |64 bits (8 bytes) de entero interpretado como decimal. Este tipo de propiedad es compatible con el tipo de moneda de Microsoft Visual Basic y es el mismo que el tipo de OLE VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valor de tipo Double que se interpreta como fecha y hora. La parte entera es la fecha y la parte fraccionaria es la hora. Este tipo de propiedad es el mismo que el tipo de OLE VT_DATE y es compatible con la representación de tiempo de Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valor SCODE; Integer de 32 bits (4 bytes) sin signo. Este tipo de propiedad es el mismo que el tipo de OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |valor booleano de 16 bits (2 bytes) donde cero equivale a **false** y distinto de cero es igual a **true**. Este tipo de propiedad es el mismo que el tipo OLE VT_BOOL.  <br/> |
|PT OBJECT  <br/> |000D  <br/> |Puntero a un objeto que implementa la interfaz **IUnknown** . Este tipo de propiedad es similar a varios tipos OLE, como VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Entero de 64 bits (8 bytes) firmado o sin firmar que usa la estructura **LARGE_INTEGER** . Este tipo de propiedad es el mismo que PT_I8 y el tipo de OLE VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Cadena de caracteres de 8 bits (2 bytes) terminada en NULL. Este tipo de propiedad es el mismo que el tipo OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Cadena de caracteres de 16 bits (2 bytes) terminada en NULL. Las propiedades con este tipo tienen el tipo de propiedad restablecido en PT_UNICODE cuando se compila con el símbolo uniCODE y PT_STRING8 cuando no se compila con el símbolo uniCODE. Este tipo de propiedad es el mismo que el tipo OLE VT_LPSTR para las propiedades PT_STRING8 y VT_LPWSTR resultantes para las propiedades PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |datos enteros de 64 bits (8 bytes) y valor de hora en forma de una estructura **FILETIME** . Este tipo de propiedad es el mismo que el tipo OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valor de estructura **CLSID** . Este tipo de propiedad es el mismo que el tipo OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Tamaño variable, un **recuento** de 16 bits (2 bytes) seguido de una estructura.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Tamaño variable, matriz de bytes que representa una o varias estructuras de restricción.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Tamaño variable, **número** de acciones (no bytes) de 16 bits (2 bytes) seguida de varias estructuras de acciones de regla.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |Valor de estructura **SBinary** , una matriz de bytes contada.  <br/> |
   
> [!NOTE]
> Para determinar el valor hexadecimal para el tipo de propiedad de varios valores, o la marca PT_MV (0x00001000) en el valor hexadecimal para el tipo de propiedad. Por ejemplo, el valor hexadecimal para PT_MV_UNICODE es 0x101F y el valor hexadecimal para PT_MV_BINARY es 0x1102. 
  

