---
title: Estructura de secuencia FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 775dc1b5fdcf40867f67fbab25879bd97de24f4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816800"
---
# <a name="fielddefinition-stream-structure"></a>Estructura de secuencia FieldDefinition

**Hace referencia a**: Outlook 
  
Una estructura de secuencia FieldDefinition contiene la definición de campo de un campo definido por el usuario, o bien un conjunto de configuración de enlace de datos de un campo integrado.
  
Se puede manipular mediante programación una estructura de secuencia FieldDefinition si la estructura contiene la definición de campo de un campo definido por el usuario. No debe intentar crear o modificar una estructura FieldDefinition si la estructura contiene opciones de configuración para un campo integrado mediante programación. Debe usar el Diseñador de formularios de Microsoft Outlook para mantener la configuración para los campos integrados.
  
> [!NOTE]
> Outlook es compatible con dos formatos de definiciones de campo: PropDefV1 y PropDefV2. El formato de PropDefV1 de definiciones de campo contiene los siguientes elementos de datos: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI y ErrorANSI. El formato de PropDefV2 contiene los mismos elementos y los elementos InternalType y SkipBlocks. 
>
> Outlook no mantiene una versión de Unicode para los elementos de datos FormulaANSI, ValidationRuleANSI y ValidationTextANSI en el formato de definición de campo de PropDefV2. Si estos elementos contienen caracteres que no sean ASCII, esos caracteres pueden interpretarse de forma incoherente dependiendo de la página de códigos ANSI del equipo donde se ejecuta Outlook. Por lo tanto, debe usar sólo los valores de cadena que se componen únicamente de caracteres ASCII para estos elementos de datos. 
  
Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden especificado a continuación.
  
- Indicadores: DWORD (4 bytes), una combinación de cero o más indicadores cuyos valores y significados se enumeran en la siguiente tabla.
    
    |**Nombre de indicador**|**Valor**|**Descripción**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |La estructura de FieldDefinition contiene una definición de un campo definido por el usuario.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Para un control de formulario enlazado a este campo, la casilla de verificación **se requiere un valor para este campo** está seleccionada en la ficha **validación** del cuadro de diálogo **Propiedades** .  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0 x 00000004  <br/> |Para un control de formulario enlazado a este campo, la casilla de verificación para **incluir este campo en impresión y guardar como** está seleccionado en la ficha **validación** del cuadro de diálogo **Propiedades** .  <br/> |
    |PDO_CALC_AUTO  <br/> |0 x 00000008  <br/> |Para un control de formulario enlazado a este campo, la casilla de verificación para **calcular esta fórmula automáticamente** está seleccionada en la ficha **valor** del cuadro de diálogo **Propiedades** .  <br/> |
    |PDO_FT_CONCAT  <br/> |0 x 00000010  <br/> |Éste es un campo de tipo de **combinación** y tiene la opción de **uniendo los campos y los fragmentos de texto con cada una de las demás** seleccionada en su cuadro de diálogo **Campo de fórmula de combinación** .  <br/> |
    |PDO_FT_SWITCH  <br/> |0 x 00000020  <br/> |Este campo es del tipo de **combinación** y ha seleccionado la opción **mostrando sólo el primer campo que contenga datos, omitiendo el resto** en el cuadro de diálogo **Campo de fórmula de combinación** .  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Esta marca no se usa en Outlook, pero se incluye para todas las definiciones de campo definido por el usuario.  <br/> |
   
- VT: WORD (2 bytes), el tipo de datos del campo, que es una constante de la enumeración [VARENUM](http://msdn.microsoft.com/en-us/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId: DWORD (4 bytes), el identificador de envío del campo. Para un campo definido por el usuario, el valor es 0.
    
- NmidNameLength: Palabra (2 bytes), el número de elementos de la matriz NmidName.
    
- NmidName: Una matriz de WCHAR. Para una definición de campo definido por el usuario, ésta es la representación de Unicode (UTF-16) del nombre del campo. El recuento de esta matriz es igual a NmidNameLength.
    
- NameANSI: Una estructura de secuencia de [PackedAnsiString](packedansistring-stream-structure.md) . Ésta es la representación de ANSI del nombre del campo. 
    
- FormulaANSI: Una estructura de secuencia de PackedAnsiString. Ésta es una representación ANSI de la fórmula de cálculo para el campo. Se muestra en la sección **Valor inicial** de la ficha **valor** del cuadro de diálogo **Propiedades** de un control de formulario enlazado a este campo. 
    
- ValidationRuleANSI: Una estructura de secuencia de PackedAnsiString. Ésta es una representación ANSI de fórmula de validación del campo. Se muestra en el cuadro de texto para la **Fórmula de validación** en la ficha **validación** del cuadro de diálogo **Propiedades** de un control de formulario enlazado a este campo. 
    
- ValidationTextANSI: Una estructura de secuencia de PackedAnsiString. Ésta es una representación ANSI de texto de error de validación del campo. Se muestra en el cuadro de texto para **Mostrar este mensaje si falla la validación** en la ficha **validación** del cuadro de diálogo **Propiedades** de un control de formulario enlazado a este campo. 
    
- ErrorANSI: Una estructura de secuencia de PackedAnsiString. Outlook no utiliza este elemento; Este elemento se debe establecer en una cadena vacía.
    
- InternalType: DWORD (4 bytes), el tipo del campo interno. Este elemento de datos está presente sólo si el formato de definición de campo es PropDefV2. El tipo interno es uno de los valores siguientes, cada uno de los cuales corresponde a un tipo en el cuadro de diálogo **Nuevo campo** para campos definidos por el usuario. 
    
    |**Nombre de tipo interno**|**Valor**|**Tipo correspondiente en el cuadro de diálogo **Nuevo campo****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Número** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Moneda  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4  <br/> |**S?/No** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Fecha y hora** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**Combinación**, con la opción **mostrando sólo el primer campo que contenga datos, omitiendo el resto** seleccionada en el cuadro de diálogo **Campo de fórmula de combinación** .  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |No se usa este tipo para campos definidos por el usuario.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |No se usa este tipo para campos definidos por el usuario.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |No se usa este tipo para campos definidos por el usuario.  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**Combinación**, con la opción **uniendo los campos y los fragmentos de texto con cada una de las demás** seleccionada en el cuadro de diálogo **Campo de fórmula de combinación** .  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Palabra clave** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks: Una serie de una o más estructuras de secuencia de [SkipBlock](skipblock-stream-structure.md) . Este elemento de datos está presente sólo si el formato de definición de campo es PropDefV2. Si el formato de definición de campo es PropDefV2, la serie debe contener al menos una estructura SkipBlock, la estructura de SkipBlock que tiene el elemento de datos de tamaño igual a 0, y debe empezar y terminar con esta estructura de SkipBlock la serie. 
    
   El propósito de una estructura SkipBlock depende de su posición relativa en la serie de SkipBlocks. Si la definición de campo está en formato PropDefV2, y la primera estructura no es la estructura de terminación (el elemento de datos de tamaño es mayor que 0), Outlook supone que la primera estructura SkipBlock especifica el nombre del campo en Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Si el primer SkipBlock es la estructura de terminación, el elemento de datos de NameANSI se usa para determinar el nombre del campo. Si dicha cadena contiene los caracteres que no sean ASCII, esos caracteres pueden interpretarse de forma incoherente dependiendo de la página de códigos ANSI del equipo donde se ejecuta Outlook. Para evitar esas incoherencias, asegúrese de que especificar siempre la primera SkipBlock en las definiciones de campo que cree, al menos cuando el nombre del campo incluye caracteres que no sean ASCII. 
  
   Si una versión futura de un formato de definición de campo presenta fragmentos adicionales de datos en la secuencia de FieldDefinition, estos datos pueden almacenarse como estructuras de secuencia de SkipBlock adicionales de la serie SkipBlocks antes de la estructura SkipBlock terminación que tiene la Elemento de datos de tamaño igual a 0. Las versiones anteriores de Outlook pueden ignorar estas estructuras de SkipBlock extra hasta la estructura SkipBlock terminación y procesar aún correctamente todos los bloques que admiten.
    
## <a name="see-also"></a>Vea también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Estructuras de secuencia](stream-structures.md)
- [Muestra de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)

