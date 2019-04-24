---
title: Estructura de la secuencia FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334898"
---
# <a name="fielddefinition-stream-structure"></a>Estructura de la secuencia FieldDefinition

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una estructura de secuencia FieldDefinition contiene la definición de campo de un campo definido por el usuario o un conjunto de opciones de configuración de enlace de datos para un campo integrado.
  
Puede manipular mediante programación una estructura de secuencia FieldDefinition si la estructura contiene la definición de campo de un campo definido por el usuario. No debe intentar crear o modificar mediante programación una estructura FieldDefinition si la estructura contiene la configuración de un campo integrado. Debe usar el diseñador de formularios de Microsoft Outlook para conservar dicha configuración en los campos integrados.
  
> [!NOTE]
> Outlook admite dos formatos de definiciones de campo: PropDefV1 y PropDefV2. El formato PropDefV1 de las definiciones de campo contiene los siguientes elementos de datos: flags, VT, dispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI y ErrorANSI. El formato PropDefV2 contiene los mismos elementos y los elementos InternalType y SkipBlocks. 
>
> Outlook no mantiene una versión Unicode para los elementos de datos FormulaANSI, ValidationRuleANSI y ValidationTextANSI en el formato de definición de campo de PropDefV2. Si estos elementos contienen caracteres que no son ASCII, dichos caracteres pueden interpretarse incoherentemente en función de la página de códigos ANSI del equipo en el que se ejecuta Outlook. Por lo tanto, solo debe usar valores de cadena que consistan exclusivamente de caracteres ASCII para estos elementos de datos. 
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden especificado a continuación.
  
- Flags: DWORD (4 bytes), una combinación de cero o más indicadores cuyos valores y significados se enumeran en la siguiente tabla.
    
    |**Nombre de marca**|**Value**|**Descripción**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |La estructura FieldDefinition contiene una definición de un campo definido por el usuario.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Para un control de formulario enlazado a este campo, la casilla de verificación de **un valor es necesaria para este campo** está seleccionada en la ficha **validación** del cuadro de diálogo **propiedades** .  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Para un control de formulario enlazado a este campo, la casilla de verificación **incluir este campo para imprimir y guardar como** está seleccionada en la ficha **validación** del cuadro de diálogo **propiedades** .  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Para un control de formulario dependiente de este campo, la casilla de verificación **calcular esta fórmula automáticamente** está seleccionada en la ficha **valor** del cuadro de diálogo **propiedades** .  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Se trata de un campo **combinado** de tipo y tiene los **campos de combinación y todos los fragmentos de texto con cada una** de las opciones seleccionadas en el cuadro de diálogo **combinación de campos de fórmula** .  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Este campo es de tipo **combinación** y ha **mostrado sólo el primer campo que no está vacío, omitiendo la siguiente** opción seleccionada en el cuadro de diálogo **combinar campo de fórmula** .  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Esta marca no se usa en Outlook, pero se incluye para todas las definiciones de campos definidos por el usuario.  <br/> |
   
- VT: WORD (2 bytes), el tipo de datos del campo, que es una constante de la enumeración [VARENUM](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId: DWORD (4 bytes), el identificador de envío del campo. Para un campo definido por el usuario, el valor es 0.
    
- NmidNameLength: WORD (2 bytes), el número de elementos de la matriz NmidName.
    
- NmidName: una matriz de WCHAR. Para una definición de campo definida por el usuario, esta es la representación Unicode (UTF-16) del nombre del campo. El recuento de esta matriz es igual a NmidNameLength.
    
- NameANSI: una estructura de secuencia [PackedAnsiString](packedansistring-stream-structure.md) . Esta es la representación ANSI del nombre del campo. 
    
- FormulaANSI: una estructura de secuencia PackedAnsiString. Es una representación ANSI de la fórmula de cálculo del campo. Se muestra en la sección **valor inicial** de la ficha **valor** del cuadro de diálogo **propiedades** de un control de formulario enlazado a este campo. 
    
- ValidationRuleANSI: una estructura de secuencia PackedAnsiString. Es una representación ANSI de la fórmula de validación del campo. Se muestra en el cuadro de texto de la **fórmula de validación** en la ficha **validación** del cuadro de diálogo **propiedades** de un control de formulario enlazado a este campo. 
    
- ValidationTextANSI: una estructura de secuencia PackedAnsiString. Esta es una representación ANSI del texto de error de validación del campo. Se muestra en el cuadro de texto para **Mostrar este mensaje si se produce un error** en la validación en la ficha **validación** del cuadro de diálogo **propiedades** de un control de formulario enlazado a este campo. 
    
- ErrorANSI: una estructura de secuencia PackedAnsiString. Outlook no utiliza este elemento; debe establecer este elemento en una cadena vacía.
    
- InternalType: DWORD (4 bytes), el tipo interno del campo. Este elemento de datos solo está presente si el formato de definición de campo es PropDefV2. El tipo Internal es uno de los siguientes valores, cada uno de los cuales corresponde a un tipo en el cuadro de diálogo **nuevo campo** para campos definidos por el usuario. 
    
    |**Nombre de tipo interno**|**Value**|**Tipo correspondiente en el cuadro de diálogo **nuevo campo****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |comprendi  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |segundo  <br/> |**Percent** <br/> |
    |Moneda  <br/> |3  <br/> |**Moneda** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Sí/No** <br/> |
    |iTypeDateTime  <br/> |2,5  <br/> |**Fecha y hora** <br/> |
    |iTypeDuration  <br/> |6,5  <br/> |**Duración** <br/> |
    |iTypeCombination  <br/> |0,7  <br/> |**Combinación**, con la opción **que muestra sólo el primer campo no vacío y** se omiten las siguientes opciones seleccionadas en el cuadro de diálogo **combinar campo de fórmula** .  <br/> |
    |iTypeFormula  <br/> |8,5  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |Este tipo no se usa para los campos definidos por el usuario.  <br/> |
    |iTypeVariant  <br/> |metros  <br/> |Este tipo no se usa para los campos definidos por el usuario.  <br/> |
    |iTypeFloatResult  <br/> |12  <br/> |Este tipo no se usa para los campos definidos por el usuario.  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**Combinación**, con los **campos de combinación y cualquier fragmento de texto con las demás** opciones seleccionadas en el cuadro de diálogo **combinar campo de fórmula** .  <br/> |
    |iTypeKeywords  <br/> |apartado  <br/> |**Palabra clave** <br/> |
    |iTypeInteger  <br/> |apartado  <br/> |**Integer** <br/> |
   
- SkipBlocks: una serie de una o varias estructuras de secuencia de [SkipBlock](skipblock-stream-structure.md) . Este elemento de datos solo está presente si el formato de definición de campo es PropDefV2. Si el formato de definición de campo es PropDefV2, la serie debe contener al menos una estructura SkipBlock, la estructura SkipBlock que tiene el elemento de datos size igual a 0 y la serie debe comenzar y terminar con esta estructura SkipBlock. 
    
   El propósito de una estructura SkipBlock depende de su posición relativa en la serie SkipBlocks. Si la definición del campo está en formato PropDefV2 y la primera estructura no es la estructura final (el elemento de datos size es mayor que 0), Outlook supone que la primera estructura SkipBlock especifica el nombre del campo en Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Si el primer SkipBlock es la estructura de terminación, el elemento de datos NameANSI se usa para determinar el nombre del campo. Si la cadena contiene caracteres que no sean ASCII, dichos caracteres pueden interpretarse incoherentemente en función de la página de códigos ANSI del equipo en el que se ejecuta Outlook. Para evitar este tipo de incoherencias, asegúrese de especificar siempre la primera SkipBlock en las definiciones de campo que cree, al menos cuando el nombre del campo incluya caracteres que no sean ASCII. 
  
   Si una versión futura de un formato de definición de campo introduce otros datos en la secuencia FieldDefinition, estos datos se pueden almacenar como estructuras de secuencia SkipBlock adicionales en la serie SkipBlocks antes de la estructura SkipBlock de terminación que tiene el El elemento de datos de tamaño es igual a 0. Las versiones anteriores de Outlook pueden omitir estas estructuras de SkipBlock adicionales hasta la estructura de terminación de SkipBlock y procesar correctamente todos los bloques que admiten.
    
## <a name="see-also"></a>Vea también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Estructuras de secuencia](stream-structures.md)
- [Estructura de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)

