---
title: Estructuras de la secuencia de campos de carpeta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385091"
---
# <a name="folder-fields-stream-structures"></a>Estructuras de la secuencia de campos de carpeta

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Propiedad de [PidTagUserFields](pidtaguserfields-canonical-property.md) de un mensaje contiene una secuencia binaria, FolderUserFields, que contiene las definiciones de campo definido por el usuario de la carpeta. En este tema se describe las estructuras de secuencia para las definiciones de campo definido por el usuario de carpeta. 

Una estructura de secuencia FolderUserFields consta de una estructura FolderUserFieldsA o una estructura FolderUserFieldsA seguido de una estructura FolderUserFieldsW.
  
Elementos de datos en esta secuencia se almacenan inmediatamente después de cada uno de los otros en el siguiente orden especificado:
  
- **FolderUserFieldsAnsi**: estructura en secuencia de un FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (opcional): estructura en secuencia de un FolderUserFieldsW.
    
Se detecta la presencia de FolderUserFieldsUnicode por la longitud total de la FolderUserFields es mayor que la longitud de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi se usa para la compatibilidad con los más antiguo, no Unicode, las versiones de los clientes MAPI, por lo tanto, si FolderUserFieldsUnicode está presente, se omite el contenido de FolderUserFieldsAnsi. Para evitar datos posibles pérdidas de paquetes en la conversión de ANSI, al crear una secuencia de FolderUserFields siempre incluyen el elemento FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Estructura de la secuencia de FolderUserFieldsA

Una estructura de secuencia de FolderUserFieldsA es una matriz de las estructuras de secuencia de FolderFieldDefinitionA que contienen definiciones para todos los campos definidos por el usuario en una carpeta de Outlook, a menos que se reemplaza por el elemento FolderUserFieldsW de la estructura FolderUserFields.
  
Elementos de datos en esta secuencia se almacenan en el orden de bytes little-endian, inmediatamente después de cada uno de los otros en el siguiente orden especificado:
  
- **FieldDefinitionCount**: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Éste es el recuento de elementos de la matriz **FieldDefinitions** .
    
- **FieldDefinitions**: una matriz de FolderFieldDefinitionA en secuencia de estructuras. El recuento de esta matriz es igual al elemento de datos de **FieldDefinitionCount** .
    
A menos que este FolderUserFieldsA se reemplaza por el elemento FolderUserFieldsW de la estructura de FolderUserFields, la matriz **FieldDefinitions** debe ser "terminada en null" al campo de Common.FieldType de su última FolderFieldDefinitionA elemento igual de tener para ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Estructura de la secuencia de FolderUserFieldsW

Una estructura de secuencia de FolderUserFieldsW es una matriz de las estructuras de secuencia de FolderFieldDefinitionW que contienen definiciones para todos los campos definidos por el usuario en una carpeta de Outlook.
  
Elementos de datos en esta secuencia se almacenan en el orden de bytes little-endian, inmediatamente después de cada uno de los otros en el siguiente orden especificado:
  
- **FieldDefinitionCount**: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Éste es el recuento de elementos de la matriz **FieldDefinitions** .
    
- **FieldDefinitions**: una matriz de FolderFieldDefinitionW en secuencia de estructuras. El recuento de esta matriz es igual al elemento de datos de **FieldDefinitionCount** .
    
La matriz de **FieldDefinitions** debe ser "terminada en null" haciendo que el campo de Common.FieldType de su última FolderFieldDefinitionW elemento igual a ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Estructura de la secuencia de FolderFieldDefinitionA

Una estructura de secuencia FolderFieldDefinitionA contiene una definición de un campo definido por el usuario con el nombre de campo que se almacenan en ANSI.
  
Elementos de datos en esta secuencia se almacenan en el orden de bytes little-endian, inmediatamente después de cada uno de los otros en el siguiente orden especificado:
  
- **FieldType**: FldType (4 bytes), el tipo de este campo.
    
- **FieldNameLength**: palabra (2 bytes), el número de elementos de la matriz **FieldName** .
    
- **FieldName**: una matriz de CHAR. Ésta es la representación de página de códigos de ANSI CP_ACP del nombre del campo. El recuento de esta matriz es igual a **FieldNameLength**. El nombre de campo debe cumplir las restricciones en el parámetro Name tal como se especifica en el método [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Outlook podrá controlar algunos valores de **FieldName** no se ajusten a estas restricciones, sin embargo tales casos no se incluyen en este tema. 
  
- **Común**: estructura en secuencia de un FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Estructura de la secuencia de FolderFieldDefinitionW

Una estructura de secuencia FolderFieldDefinitionW contiene una definición de un campo definido por el usuario con el nombre de campo que se almacenan en Unicode.
  
Elementos de datos en esta secuencia se almacenan en el orden de bytes little-endian, inmediatamente después de cada uno de los otros en el siguiente orden especificado:
  
- **FieldType**: FldType (4 bytes), el tipo de este campo.
    
- **FieldNameLength**: palabra (2 bytes), el número de elementos de la matriz **FieldName** .
    
- **FieldName**: una matriz de WCHAR. Ésta es la representación de Unicode (UTF-16) del nombre del campo. El recuento de esta matriz es igual a **FieldNameLength**. El nombre de campo debe cumplir las restricciones en el parámetro Name tal como se especifica en el método [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Outlook puede ser capaz de controlar algunos valores de **FieldName** no se ajusten a estas restricciones, pero estos casos no se incluyen en este tema. 
  
- **Común**: estructura en secuencia de un FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>FldType (enumeración)

Valores de la enumeración **FldType** se enumeran en la siguiente tabla. 
  
|Nombre|Valor|Significado|
|:-----|:-----|:-----|
|ftNull  <br/> |0 x 0  <br/> |Este tipo de campo se usa para una matriz de definiciones de campo termine en null.  <br/> |
|ftString  <br/> |0 x 1  <br/> |Texto  <br/> |
|ftInteger  <br/> |0 x 3  <br/> |Entero  <br/> |
|ftTime  <br/> |0 x 5  <br/> |Fecha y hora  <br/> |
|ftBoolean  <br/> |0 x 6  <br/> |Sí/No  <br/> |
|ftDuration  <br/> |0 x 7  <br/> |Duración  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Keywords  <br/> |
|ftFloat  <br/> |0xC  <br/> |Número o porcentaje  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Moneda  <br/> |
|ftCalc  <br/> |0 x 12  <br/> |Fórmula  <br/> |
|ftSwitch  <br/> |0 x 13  <br/> |Combinación de tipo mostrando sólo el primer campo que contenga datos-omitiendo el resto.  <br/> |
|ftConcat  <br/> |0 x 17  <br/> |Combinación de tipo uniendo los campos y los fragmentos de texto entre sí.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Estructura de la secuencia de FolderFieldDefinitionCommon

Una estructura de secuencia FolderFieldDefinitionCommon contiene los datos de una definición de campo definido por el usuario que es común a un FolderFieldDefinitionA y un FolderFieldDefinitionW.
  
Elementos de datos en esta secuencia se almacenan en el orden de bytes little-endian, inmediatamente después de cada uno de los otros en el siguiente orden especificado:
  
- **PropSetGuid**: GUID (16 bytes), la propiedad GUID del nombre de propiedad MAPI correspondiente del campo de la carpeta del conjunto. Valor de este campo debe ser igual a PS_PUBLIC_STRINGS, a menos que el tipo de campo es **ftNone** , en cuyo caso el valor de este campo debe ser igual a GUID_NULL. 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Outlook podrá controlar algunos valores de **PropSetGuid** no se ajusten a esta restricción, sin embargo tales casos no se incluyen en este tema. 
  
- **fcapm**: DWORD (4 bytes), una combinación de cero o más indicadores de los valores de que y significados se enumeran en la siguiente tabla. Marcas con el mismo valor tienen significados dependientes en el tipo del campo, es decir, el valor de FldType.
    
    |Nombre de indicador|Valor|Significado|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |El campo es modificable.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |El campo es se puede ordenar.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0 x 00000004  <br/> |El campo es agrupable.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0 x 00000100  <br/> |El campo puede contener varias líneas de texto.  <br/> |
    |FCAPM_PERCENT  <br/> |0 x 01000000  <br/> |En este campo de la ftFloat de tipo es un campo de porcentaje.  <br/> |
    |FCAPM_DATEONLY  <br/> |0 x 01000000  <br/> |En este campo de la ftTime de tipo es un campo de tiempo sólo de fecha.  <br/> |
    |FCAPM_UNITLESS  <br/> |0 x 01000000  <br/> |Para este campo de la ftInteger de tipo, no hay ninguna unidad está permitida en formato de presentación; Por ejemplo formatos como "equipo - 640 K..." no se permiten.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0 x 80000000  <br/> |Se puede editar el campo en el elemento: se trata específicamente de formularios personalizados.  <br/> |
   
- **dwString**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **dwBitmap**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **dwDisplay**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **iFmt**: INT (4 bytes). Para los tipos de campo que tienen el "formato:" cuadro combinado en el "nuevo campo de", "Editar campo" y "Propiedades de campo" cuadros de diálogo, el índice basado en 0 del formato seleccionado en dicho cuadro combinado. Para los tipos de campo sin dicho cuadro combinado, este debe ser 0. El valor del campo junto con el tipo de campo identifica de forma exclusiva determinar los valores de la **dwString**, **dwBitmap**, y campos de **dwDisplay** , vea la primera nota siguiente.
    
- **wszFormulaLength**: palabra (2 bytes), el número de elementos de la matriz **wszFormulaLength** .
    
- **wszFormulaLength**: una matriz de WCHAR. Ésta es la representación de Unicode (UTF-16) de la cadena de fórmula del campo en su formato estándar. Vea la nota siguiente segundo para la descripción del estándar y los formatos de la interfaz de usuario de fórmula de un campo. El recuento de esta matriz es igual a **wszFormulaLength**. La cadena de fórmula debe ser una cadena vacía a menos que el tipo de campo es **ftCalc**, **ftSwitch** o **ftConcat**.
    
> [!NOTE]
> Aunque los valores de **dwString**, **dwBitmap**y **dwDisplay** identifica de forma exclusiva se determina según el valor de **FldType** y el valor **iFmt** , que son redundantes, sus valores correctos siguen siendo necesarios para correcta procesamiento de la definición de campo por Outlook. No hay ninguna descripción sencilla del algoritmo que lleva a cabo esta determinación. 
> 
> Por lo tanto, para averiguar qué valores **dwString**, **dwBitmap**y **dwDisplay** corresponden a un determinado valor de **FldType** y un valor de **iFmt** , realizar una prueba mediante la creación de un campo definido por el usuario de ese tipo y con ese formato seleccionado en el cuadro combinado de **formato** , suponiendo que su aplicación, inspeccionar la secuencia **FolderUserFields** resultante que crea Outlook para ese campo definido por el usuario. 
  
Se edita la fórmula del campo en su formato de la interfaz de usuario en el cuadro de texto de la **fórmula** del **Campo nuevo**, **Editar campo**y cuadros de diálogo de **Propiedades de campo** para el campo definido por el usuario. El algoritmo para convertir una fórmula desde el formato de la interfaz de usuario en el formato estándar depende del tipo de campo tal como se describe en el siguiente: 
- Para los campos de tipos **ftCalc** y **ftSwitch**, el formato estándar para los campos integrados, ya que las propiedades MAPI correspondientes no son las propiedades con nombre de la MNID kind\_cadena, se obtiene mediante el reemplazo de fragmentos de nombre de campo, es decir `[<field_name>]` con fragmentos de `[_<field_dispid_decimal>]`. 

  Por ejemplo, si el formato de la interfaz de usuario de una fórmula para un campo del tipo de **fórmula**, que es **ftCalc**, con el idioma de la interfaz de usuario de Office que se va a inglés de Estados Unidos, es `[Business Phone] & [My custom field]`, donde `My custom field` es el nombre de un campo definido por el usuario, el formato estándar de una fórmula de este tipo sería `[_14856] & [My custom field]`.

- Para los campos de la de tipo **ftConcat**, se obtiene el formato estándar, realice lo siguiente:

  1. Truncar el espacio en blanco inicial y final. 
  2. Analizar la fórmula en una secuencia de fragmentos de los dos tipos siguientes: 
     - Un nombre de campo entre corchetes, es decir, `[<field_name>]`. 
     - Una subcadena que no contiene ningún corchetes.   
      Asegurarse de que no hay dos fragmentos del segundo tipo son adyacentes en la secuencia. Si la fórmula no se puede analizar de este modo, se considera no válido. 
  3. Lleve a cabo la sustitución de la misma para los fragmentos del primer tipo en cuanto a los campos **ftCalc** y **ftSwitch** . 
  4. Para cada fragmento del segundo tipo, escape todas las comillas dobles ("" ") caracteres, si lo hay, con dos caracteres de comillas dobles consecutivos y escríbalo entre comillas dobles. 
  5. Insertar una cadena de y comercial (`&`) entre cada par de fragmentos adyacentes.
 
  Por ejemplo, con el idioma de la interfaz de usuario de Office inglés de Estados Unidos, si el formato de la interfaz de usuario de una fórmula para un campo del tipo **ftConcat** es `text1 [Business Phone] "text2" [My custom field]`, donde `My custom field` es el nombre de un campo definido por el usuario, el formato estándar para una fórmula de este tipo sería `""text1" & [_14856] & """text2""" & [My custom field]"`. 
  
## <a name="see-also"></a>Vea también

- [Muestra de la secuencia FolderUserFields](folderuserfields-stream-sample.md)
- [Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)

