---
title: Estructura de secuencias FieldDefinition
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
# <a name="fielddefinition-stream-structure"></a>Estructura de secuencias FieldDefinition

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una estructura de secuencias FieldDefinition contiene la definición de campo de un campo definido por el usuario o un conjunto de configuraciones de enlace de datos para un campo integrado.
  
Puede manipular mediante programación una estructura de secuencia FieldDefinition si la estructura contiene la definición de campo de un campo definido por el usuario. No debe intentar crear o modificar mediante programación una estructura FieldDefinition si la estructura contiene la configuración de un campo integrado. Debe usar el Diseñador de formularios de Microsoft Outlook para mantener dicha configuración para los campos integrados.
  
> [!NOTE]
> Outlook admite dos formatos de definiciones de campo: PropDefV1 y PropDefV2. El formato PropDefV1 de las definiciones de campo contiene los siguientes elementos de datos: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI y ErrorANSI. El formato PropDefV2 contiene los mismos elementos y los elementos InternalType y SkipBlocks. 
>
> Outlook no mantiene una versión Unicode para los elementos de datos FormulaANSI, ValidationRuleANSI y ValidationTextANSI en el formato de definición de campo PropDefV2. Si estos elementos contienen caracteres que no son ASCII, dichos caracteres pueden interpretarse de forma incoherente en función de la página de códigos ANSI del equipo en el que se ejecuta Outlook. Por lo tanto, solo debe usar valores de cadena que se componen completamente de caracteres ASCII para estos elementos de datos. 
  
Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el orden especificado a continuación.
  
- Marcas: DWORD (4 bytes), una combinación de cero o más marcas cuyos valores y significados se enumeran en la tabla siguiente.
    
    |**Nombre de la marca**|**Valor**|**Descripción**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |La estructura FieldDefinition contiene una definición de un campo definido por el usuario.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Para un control de formulario enlazado a este campo, la casilla de  verificación **de un** valor A es necesaria para este campo está seleccionada en la ficha Validación del cuadro **de** diálogo Propiedades.  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Para un control de formulario enlazado a este campo, la casilla de  verificación Incluir este campo para imprimir y Guardar **como** está seleccionada en la ficha Validación del cuadro **de** diálogo Propiedades.  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Para un control de formulario enlazado a  este campo, la casilla calcular esta fórmula automáticamente se activa en la ficha **Valor** del cuadro **de** diálogo Propiedades.  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Se trata de un campo de tipo **Combination** y tiene los campos de unión y los fragmentos de texto **seleccionados** en el cuadro de diálogo Campo de fórmula **combinada.**  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Este campo es de tipo **Combination** y tiene la opción Mostrar solo el primer campo no **vacío,** ignorando los siguientes seleccionados en el cuadro de diálogo Campo de fórmula **combinada.**  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Outlook no usa esta marca, pero se incluye para todas las definiciones de campo definidas por el usuario.  <br/> |
   
- VT: WORD (2 bytes), el tipo de datos del campo, que es una constante de la enumeración [VARENUM.](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) 
    
- DispId: DWORD (4 bytes), el identificador de envío del campo. Para un campo definido por el usuario, el valor es 0.
    
- NmidNameLength: WORD (2 bytes), el número de elementos de la matriz NmidName.
    
- NmidName: una matriz de WCHAR. Para una definición de campo definida por el usuario, se trata de la representación Unicode (UTF-16) del nombre del campo. El recuento de esta matriz es igual a NmidNameLength.
    
- NameANSI: una [estructura de secuencias PackedAnsiString.](packedansistring-stream-structure.md) Esta es la representación ANSI del nombre del campo. 
    
- FormulaANSI: una estructura de secuencias PackedAnsiString. Se trata de una representación ANSI de la fórmula de cálculo para el campo. Se muestra en la sección  **Valor** inicial  de la ficha Valor del cuadro de diálogo Propiedades de un control de formulario enlazado a este campo. 
    
- ValidationRuleANSI: una estructura de secuencias PackedAnsiString. Se trata de una representación ANSI de la fórmula de validación del campo. Se muestra en el cuadro de  texto **de**  Fórmula de validación en la ficha Validación del cuadro de diálogo Propiedades de un control de formulario enlazado a este campo. 
    
- ValidationTextANSI: una estructura de secuencias PackedAnsiString. Se trata de una representación ANSI del texto de error de validación del campo. Se muestra en el cuadro de texto para Mostrar  este mensaje  si se produce un error en la validación en la ficha Validación del cuadro de diálogo Propiedades de un control de formulario enlazado a este campo.  
    
- ErrorANSI: una estructura de secuencias PackedAnsiString. Outlook no usa este elemento; debes establecer este elemento en una cadena vacía.
    
- InternalType: DWORD (4 bytes), el tipo interno del campo. Este elemento de datos solo está presente si el formato de definición de campo es PropDefV2. El tipo interno es uno de los siguientes valores, cada  uno de los cuales corresponde a un tipo en el cuadro de diálogo Nuevo campo para los campos definidos por el usuario. 
    
    |**Nombre de tipo interno**|**Valor**|**Tipo correspondiente en el **cuadro de diálogo Nuevo** campo**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1   <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2   <br/> |**Percent** <br/> |
    |Divisa  <br/> |3   <br/> |**Moneda** <br/> |
    |iTypeBool  <br/> |4   <br/> |**Sí/No** <br/> |
    |iTypeDateTime  <br/> |5   <br/> |**Fecha y hora** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duración** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**Combinación**, con el campo Mostrar solo el primer campo no **vacío,** ignorando los siguientes seleccionados en el cuadro de diálogo Campo de **fórmula combinada.**  <br/> |
    |iTypeFormula  <br/> |8   <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9   <br/> |Este tipo no se usa para campos definidos por el usuario.  <br/> |
    |iTypeVariant  <br/> |10    <br/> |Este tipo no se usa para campos definidos por el usuario.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Este tipo no se usa para campos definidos por el usuario.  <br/> |
    |iTypeConcat  <br/> |12   <br/> |**Combinación**, con los **campos de unión y los fragmentos** de texto seleccionados entre sí en el cuadro de diálogo Campo de **fórmula** combinada.  <br/> |
    |iTypeKeywords  <br/> |13   <br/> |**Palabra clave** <br/> |
    |iTypeInteger  <br/> |14   <br/> |**Integer** <br/> |
   
- SkipBlocks: una serie de una o varias estructuras de flujo [SkipBlock.](skipblock-stream-structure.md) Este elemento de datos solo está presente si el formato de definición de campo es PropDefV2. Si el formato de definición de campo es PropDefV2, la serie debe contener al menos una estructura SkipBlock, la estructura SkipBlock que tiene el elemento de datos Size igual a 0, y la serie debe comenzar y terminar con esta estructura SkipBlock. 
    
   El propósito de una estructura SkipBlock depende de su posición relativa en la serie SkipBlocks. Si la definición de campo está en formato PropDefV2 y la primera estructura no es la estructura de terminación (el elemento de datos Size es mayor que 0), Outlook supone que la primera estructura SkipBlock especifica el nombre del campo en Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Si el primer SkipBlock es la estructura de terminación, se usa el elemento de datos NameANSI para determinar el nombre del campo. Si esa cadena contiene caracteres que no sean ASCII, dichos caracteres pueden interpretarse de forma incoherente en función de la página de códigos ANSI del equipo en el que se ejecuta Outlook. Para evitar este tipo de incoherencias, asegúrese de especificar siempre el primer SkipBlock en las definiciones de campo que cree, al menos cuando el nombre del campo incluya caracteres que no sean ASCII. 
  
   Si una versión futura de un formato de definición de campo introduce fragmentos de datos adicionales en la secuencia FieldDefinition, estos datos se pueden almacenar como estructuras de flujo SkipBlock adicionales en la serie SkipBlocks antes de la estructura SkipBlock de finalización que tiene el elemento de datos Size igual a 0. Las versiones anteriores de Outlook pueden omitir estas estructuras SkipBlock adicionales de forma segura hasta la estructura SkipBlock de terminación y seguir procesando correctamente todos los bloques que admiten.
    
## <a name="see-also"></a>Consulte también

- [Elementos y campos de Outlook](outlook-items-and-fields.md)
- [Estructuras de flujo](stream-structures.md)
- [Estructura de secuencia PropertyDefinition](propertydefinition-stream-structure.md)

