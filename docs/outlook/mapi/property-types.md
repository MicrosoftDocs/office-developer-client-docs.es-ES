---
title: Tipos de propiedad
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
# <a name="property-types"></a>Tipos de propiedad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI admite propiedades de valor único y de varios valores. Con una propiedad de valor único, hay un valor del tipo base para la propiedad. Con una propiedad de varios valores, hay varios valores del tipo base. 
  
Los tipos de propiedades de valor único y de varios valores compatibles con MAPI se describen en la tabla siguiente. Para cada tipo de valor único que tenga un tipo de valor múltiple correspondiente, el tipo de valor múltiple aparece entre paréntesis después del tipo de valor único.
  
|**Tipo de propiedad**|**Valor hexadecimal**|**Descripción**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indica que el tipo de propiedad es desconocido. Este tipo de propiedad está reservado para su uso con métodos de interfaz.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Indica que no hay ningún valor de propiedad. Este tipo de propiedad está reservado para su uso con métodos de interfaz y es el mismo que el tipo OLE VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Entero de 16 bits (2 bytes) firmado. Este tipo de propiedad es el mismo que PT_SHORT (PT_MV_SHORT) y el tipo OLE VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Entero de 32 bits (4 bytes) firmado o sin firmar. Este tipo de propiedad es el mismo que PT_LONG (PT_MV_LONG) y el tipo OLE VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |Valor de punto flotante de 32 bits (8 bytes). Este tipo de propiedad es el mismo que PT_R4 (PT_MV_R4) y el tipo OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |Valor de punto flotante de 64 bits (8 bytes). Este tipo de propiedad es el mismo que PT_R8 y los tipos OLE VT_R8 y VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY )  <br/> |0006  <br/> |Entero de 64 bits (8 bytes) interpretado como decimal. Este tipo de propiedad es compatible con el tipo CURRENCY de Microsoft Visual Basic y es el mismo que el tipo OLE VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valor double que se interpreta como fecha y hora. La parte entera es la fecha y la parte de fracción es la hora. Este tipo de propiedad es el mismo que el tipo OLE VT_DATE y es compatible con la representación de Visual Basic tiempo de Microsoft.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valor SCODE; Entero sin signo de 32 bits (4 bytes). Este tipo de propiedad es el mismo que el tipo OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |Valor booleano de 16 bits (2 bytes) donde cero es igual a **false** y que no es cero es **true**. Este tipo de propiedad es el mismo que el tipo OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Puntero a un objeto que implementa la **interfaz IUnknown.** Este tipo de propiedad es similar a varios tipos OLE, como VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Entero de 64 bits (8 bytes) firmado o **sin firmar** que usa la LARGE_INTEGER estructura. Este tipo de propiedad es el mismo que PT_I8 y el tipo OLE VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Cadena de caracteres de 8 bits (2 bytes) terminada en null. Este tipo de propiedad es el mismo que el tipo OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Cadena de caracteres de 16 bits (2 bytes) terminada en null. Las propiedades con este tipo tienen el tipo de propiedad restablecido a PT_UNICODE al compilar con el símbolo UNICODE y a PT_STRING8 cuando no se compila con el símbolo UNICODE. Este tipo de propiedad es el mismo que el tipo OLE VT_LPSTR para las propiedades PT_STRING8 resultantes y VT_LPWSTR propiedades PT_UNICODE propiedades  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |Datos enteros de 64 bits (8 bytes) y valor de tiempo en forma de una **estructura FILETIME.** Este tipo de propiedad es el mismo que el tipo OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**Valor de estructura CLSID.** Este tipo de propiedad es el mismo que el tipo OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Tamaño variable, un COUNT de 16 bits (2 **bytes)** seguido de una estructura.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Tamaño variable, una matriz de bytes que representa una o más estructuras de restricción.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Tamaño variable, un COUNT de acciones de 16 bits (2 **bytes)** (no bytes) seguido de muchas estructuras de acción de regla.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**Valor de estructura SBinary,** una matriz de bytes contada.  <br/> |
   
> [!NOTE]
> Para determinar el valor Hexadecimal para el tipo de propiedad multivalor, O la marca PT_MV (0x00001000) al valor Hexadecimal para el tipo de propiedad. Por ejemplo, el valor Hexadecimal para PT_MV_UNICODE es 0x101F y el valor Hexadecimal para PT_MV_BINARY es 0x1102. 
  

