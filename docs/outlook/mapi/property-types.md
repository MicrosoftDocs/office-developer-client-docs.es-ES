---
title: Tipos de propiedad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fd0f25f20c9e628a80d27f2b70e01dacc98229b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820463"
---
# <a name="property-types"></a>Tipos de propiedad

  
  
**Se aplica a**: Outlook 
  
MAPI es compatible con propiedades de valor único y de varios valores. Con una propiedad de valor único, hay un valor del tipo base para la propiedad. Con una propiedad de varios valores, hay varios valores del tipo base. 
  
Los tipos de valor único y de varios valores de propiedad que es compatible con MAPI se describen en la siguiente tabla. Para cada tipo de valor único que tiene un tipo correspondiente de varios valores, el tipo de valor de varios aparece entre paréntesis después el tipo de valor único.
  
|**Tipo de propiedad**|**Valor hexadecimal**|**Descripción**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indica que se desconoce el tipo de propiedad. Este tipo de propiedad está reservado para su uso con los métodos de interfaz.  <br/> |
|PT_NULL  <br/> |0001  <br/> |No indica ningún valor de la propiedad. Este tipo de propiedad está reservada para uso con los métodos de interfaz y es que el mismo que el OLE escriba VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Entero con signo de 16 bits (2 bytes). Este tipo de propiedad es el mismo como PT_SHORT (PT_MV_SHORT) y OLE escriba VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Entero de 32 bits (4 bytes) con o sin signo. Este tipo de propiedad es el mismo como PT_LONG (PT_MV_LONG) y OLE escriba VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |valor punto flotante de 32 bits (8 bytes). Este tipo de propiedad es el mismo que PT_R4 (PT_MV_R4) y el tipo OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |valor punto flotante de 64 bits (8 bytes). Este tipo de propiedad es el mismo que PT_R8 y los tipos OLE VT_R8 y VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |entero de 64 bits (8 bytes) se interpreta como decimal. Este tipo de propiedad es compatible con el tipo de moneda de Microsoft Visual Basic y es que el mismo que el OLE escriba VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valor de tipo Double que se interpreta como fecha y hora. La parte entera es la fecha y la parte fraccionaria es la hora. Este tipo de propiedad es el mismo que el tipo OLE VT_DATE y es compatible con la representación de tiempo de Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valor SCODE; entero sin signo de 32 bits (4 bytes). Este tipo de propiedad es el mismo que el tipo OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |16 bits (2 bytes) valor booleano donde cero es igual a **false** y distinto de cero es igual a **true**. Este tipo de propiedad es el mismo que el tipo OLE VT_BOOL.  <br/> |
|PT OBJECT  <br/> |D. 000  <br/> |Puntero a un objeto que implementa la interfaz **IUnknown** . Este tipo de propiedad es similar a varios tipos OLE como VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Entero con signo o sin signo 64 bits (8 bytes) que usa la estructura **LARGE_INTEGER** . Este tipo de propiedad es el mismo como PT_I8 y OLE tipo VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Cadena de caracteres (2 bytes) de 8 bits terminada en null. Este tipo de propiedad es el mismo que el tipo OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Cadena terminada en null carácter de 16 bits (2 bytes). Las propiedades con este tipo de tienen el tipo de propiedad restablecer a PT_UNICODE cuando se compila con el símbolo de UNICODE y a PT_STRING8 cuando no compilar con el símbolo de UNICODE. Este tipo de propiedad es el mismo que el tipo OLE VT_LPSTR para las propiedades de PT_STRING8 resultantes y VT_LPWSTR propiedades PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |entero de 64 bits (8 bytes) fecha y hora de valor con el formato de una estructura **FILETIME** . Este tipo de propiedad es el mismo que el tipo OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valor de la estructura **CLSID** . Este tipo de propiedad es el mismo que el tipo OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Tamaño variable, un (2 bytes) de 16 bits **recuento** seguido de una estructura.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Tamaño variable, una matriz de bytes que representa una o más estructuras de restricción.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Tamaño variable, un de 16 bits (2 bytes) **recuento** de acciones (no bytes) seguido por el muchas de las estructuras de la acción de regla.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |Valor de la estructura de **SBinary** , una matriz de bytes contada.  <br/> |
   
> [!NOTE]
> Para determinar el valor hexadecimal para el tipo de propiedad de varios valores, o la PT_MV escriba marca (0 x 00001000) para el valor hexadecimal de la propiedad. Por ejemplo, el valor hexadecimal para PT_MV_UNICODE es 0x101F y el valor hexadecimal para PT_MV_BINARY es 0 x 1102. 
  

