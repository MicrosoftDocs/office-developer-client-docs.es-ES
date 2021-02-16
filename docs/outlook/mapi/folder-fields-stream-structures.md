---
title: Estructuras de secuencia de campos de carpeta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336893"
---
# <a name="folder-fields-stream-structures"></a>Estructuras de secuencia de campos de carpeta

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La propiedad [PidTagUserFields](pidtaguserfields-canonical-property.md) de un mensaje contiene una secuencia binaria, FolderUserFields, que contiene las definiciones de campo definidas por el usuario de la carpeta. En este tema se describen las estructuras de secuencia para las definiciones de campo definidas por el usuario de carpeta. 

Una estructura de secuencias FolderUserFields consta de una estructura FolderUserFieldsA o una estructura FolderUserFieldsA seguida de una estructura FolderUserFieldsW.
  
Los elementos de datos de esta secuencia se almacenan inmediatamente siguiendo los unos a los otros en el siguiente orden especificado:
  
- **FolderUserFieldsAnsi**: una estructura de secuencias FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (opcional): una estructura de secuencias FolderUserFieldsW.
    
La presencia de FolderUserFieldsUnicode se detecta por la longitud total de FolderUserFields siendo mayor que la longitud de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi se usa para la compatibilidad con versiones anteriores, no Unicode, de clientes MAPI, por lo tanto, si FolderUserFieldsUnicode está presente, se omite el contenido de FolderUserFieldsAnsi. Para evitar la posible pérdida de datos en la conversión ANSI, al crear una secuencia FolderUserFields, incluya siempre la parte FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Estructura de secuencias FolderUserFieldsA

Una estructura de secuencias FolderUserFieldsA es una matriz de estructuras de secuencia FolderFieldDefinitionA que contienen definiciones para todos los campos definidos por el usuario en una carpeta de Outlook, a menos que se invalide por la parte FolderUserFieldsW de la estructura FolderUserFields.
  
Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el siguiente orden especificado:
  
- **FieldDefinitionCount**: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Este es el recuento de elementos de la **matriz FieldDefinitions.**
    
- **FieldDefinitions:** una matriz de estructuras de secuencias FolderFieldDefinitionA. El recuento de esta matriz es igual al elemento de datos **FieldDefinitionCount.**
    
A menos que la parte FolderUserFieldsW de la estructura FolderUserFields invalide esta folderUserFieldsA, la matriz **FieldDefinitions** debe ser "terminada en null" al tener el último campo Common.FieldType del elemento FolderFieldDefinitionA igual a ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Estructura de secuencias FolderUserFieldsW

Una estructura de secuencias FolderUserFieldsW es una matriz de estructuras de secuencias FolderFieldDefinitionW que contienen definiciones para todos los campos definidos por el usuario en una carpeta de Outlook.
  
Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el siguiente orden especificado:
  
- **FieldDefinitionCount**: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Este es el recuento de elementos de la **matriz FieldDefinitions.**
    
- **FieldDefinitions:** una matriz de estructuras de secuencias FolderFieldDefinitionW. El recuento de esta matriz es igual al elemento de datos **FieldDefinitionCount.**
    
La **matriz FieldDefinitions** debe ser "terminada en null" haciendo que el último campo Common.FieldType del elemento FolderFieldDefinitionW sea igual a ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Estructura de secuencias FolderFieldDefinitionA

Una estructura de secuencia FolderFieldDefinitionA contiene una definición de un campo definido por el usuario con el nombre del campo almacenado en ANSI.
  
Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el siguiente orden especificado:
  
- **FieldType**: FldType (4 bytes), el tipo de este campo.
    
- **FieldNameLength**: WORD (2 bytes), el número de elementos de la matriz **FieldName.**
    
- **FieldName:** una matriz de CHAR. Esta es la representación ansi CP_ACP página de códigos del nombre del campo. El recuento de esta matriz es igual **a FieldNameLength**. El nombre del campo debe satisfacer las restricciones del parámetro Name, tal como se especifica en el [método UserProperties.Add.](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Es posible que Outlook pueda controlar algunos valores **fieldName** que no cumplen estas restricciones, pero estos casos no se tratan en este tema. 
  
- **Común:** una estructura de secuencias FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Estructura de secuencias FolderFieldDefinitionW

Una estructura de secuencias FolderFieldDefinitionW contiene una definición de un campo definido por el usuario con el nombre de campo almacenado en Unicode.
  
Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el siguiente orden especificado:
  
- **FieldType**: FldType (4 bytes), el tipo de este campo.
    
- **FieldNameLength**: WORD (2 bytes), el número de elementos de la matriz **FieldName.**
    
- **FieldName:** una matriz de WCHAR. Esta es la representación Unicode (UTF-16) del nombre del campo. El recuento de esta matriz es igual **a FieldNameLength**. El nombre del campo debe satisfacer las restricciones del parámetro Name, tal como se especifica en el [método UserProperties.Add.](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Outlook puede controlar algunos valores **fieldName** que no cumplen estas restricciones, pero estos casos no se tratan en este tema. 
  
- **Común:** una estructura de secuencias FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>FldType (enumeración)

**Los valores de enumeración FldType** se enumeran en la tabla siguiente. 
  
|Nombre|Valor|Significado|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Este tipo de campo se usa para finalizar en null una matriz de definiciones de campo.  <br/> |
|ftString  <br/> |0x1  <br/> |Texto  <br/> |
|ftInteger  <br/> |0x3  <br/> |Entero  <br/> |
|ftTime  <br/> |0x5  <br/> |Fecha y hora  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Sí/No  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duración  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Palabras clave  <br/> |
|ftFloat  <br/> |0xC  <br/> |Número o porcentaje  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Divisa  <br/> |
|ftCalc  <br/> |0x12  <br/> |Fórmula  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinación de tipo que muestra solo el primer campo no vacío, ignorando los siguientes.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinación de tipos que unen campos y fragmentos de texto entre sí.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Estructura de secuencias FolderFieldDefinitionCommon

Una estructura de secuencias FolderFieldDefinitionCommon contiene los datos de una definición de campo definida por el usuario que es común tanto a folderFieldDefinitionA como a FolderFieldDefinitionW.
  
Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el siguiente orden especificado:
  
- **PropSetGuid:** GUID (16 bytes), el GUID del conjunto de propiedades del nombre de propiedad MAPI correspondiente del campo de carpeta. El valor de este campo debe ser igual a PS_PUBLIC_STRINGS, a menos que el tipo de campo sea **ftNone,** en cuyo caso el valor de este campo debe ser igual a GUID_NULL. 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Es posible que Outlook pueda controlar algunos valores **propSetGuid** que no cumplen esta restricción, pero estos casos no se tratan en este tema. 
  
- **fcapm**: DWORD (4 bytes), una combinación de cero o más marca los valores de los cuales y los significados se enumeran en la tabla siguiente. Las marcas con el mismo valor tienen significados que dependen del tipo del campo, es decir, el valor FldType.
    
    |Nombre de la marca|Valor|Significado|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |El campo se puede editar.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |El campo se puede ordenar.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |El campo se puede agrupar.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |El campo puede contener varias líneas de texto.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Este campo del tipo ftFloat es un campo de porcentaje.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Este campo del tipo ftTime es un campo de fecha y hora.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Para este campo del tipo ftInteger, no se permite ninguna unidad en formato de presentación; por ejemplo, formatos como "Equipo - 640 K..." no se permiten.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |El campo se puede editar en el elemento: esto es específicamente para formularios personalizados.  <br/> |
   
- **dwString**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **dwBitmap**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **dwDisplay**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **iFmt**: INT (4 bytes). Para los tipos de campo que tienen el cuadro combinado "Formato:" en los cuadros de diálogo "Nuevo campo", "Editar campo" y "Propiedades del campo", el índice basado en 0 del formato seleccionado en ese cuadro combinado. Para los tipos de campo sin ese cuadro combinado, debe ser 0. El valor del campo junto con el tipo de campo determinan de forma única los valores de los campos **dwString**, **dwBitmap** y **dwDisplay,** consulta la primera nota siguiente.
    
- **wszFormulaLength**: WORD (2 bytes), el número de elementos de la matriz **wszFormulaLength.**
    
- **wszFormulaLength:** una matriz de WCHAR. Se trata de la representación Unicode (UTF-16) de la cadena de fórmula del campo en su formato estándar. Consulta la segunda nota siguiente para obtener la descripción de los formatos estándar y de interfaz de usuario de la fórmula de un campo. El recuento de esta matriz es igual a **wszFormulaLength**. La cadena de fórmula debe ser una cadena vacía a menos que el tipo de campo **sea ftCalc**, **ftSwitch** **o ftConcat**.
    
> [!NOTE]
> Aunque los valores de **dwString**, **dwBitmap** y **dwDisplay** se determinan de forma única en función del valor **fldType** y el valor **de iFmt,** que son redundantes, sus valores correctos siguen siendo necesarios para el procesamiento correcto de la definición de campo por parte de Outlook. No hay una descripción sencilla del algoritmo que realiza esta determinación. 
> 
> Por lo tanto, para averiguar qué valores  **dwString**, **dwBitmap** y **dwDisplay** corresponden a un valor **fldType** y un valor de **iFmt** determinados, realice una prueba creando un campo definido por el usuario de ese tipo y con ese formato seleccionado en el cuadro combinado Formato, suponiendo su aplicabilidad, inspeccione la secuencia **FolderUserFields** resultante que Outlook crea para ese campo definido por el usuario. 
  
La fórmula del campo en su formato  de interfaz de usuario se edita en el cuadro de texto Fórmula de los cuadros de diálogo Nuevo **campo,** Editar campo y Propiedades del campo para el campo definido por el usuario.  El algoritmo para convertir una fórmula del formato de interfaz de usuario al formato estándar depende del tipo de campo tal como se describe a continuación: 
- Para los campos de tipos **ftCalc** y **ftSwitch**, el formato estándar para los campos integrados, que las propiedades MAPI correspondientes no son propiedades con nombre del tipo MNID STRING, se obtiene reemplazando los fragmentos de nombre de campo, es decir, con \_ `[<field_name>]` fragmentos `[_<field_dispid_decimal>]` . 

  Por ejemplo, si el formato de interfaz de usuario de una fórmula para un campo del tipo **Fórmula**, es decir **ftCalc**, con el idioma de la interfaz de usuario de Office en inglés (EE.UU.), es , donde es el nombre de un campo definido por el `[Business Phone] & [My custom field]` usuario, el formato estándar de dicha fórmula sería `My custom field` `[_14856] & [My custom field]` .

- Para los campos del tipo **ftConcat**, el formato estándar se obtiene realizando lo siguiente:

  1. Truncar los espacios en blanco iniciales y finales. 
  2. Analice la fórmula en una secuencia de fragmentos de los dos tipos siguientes: 
     - Un nombre de campo entre corchetes, es decir, `[<field_name>]` . 
     - Una subcadena que no contiene corchetes.   
      Asegúrese de que no hay dos fragmentos del segundo tipo adyacentes en la secuencia. Si la fórmula no se puede analizar de esta forma, se considera no válida. 
  3. Realice el mismo reemplazo para los fragmentos del primer tipo que para los **campos ftCalc** **y ftSwitch.** 
  4. Para cada fragmento del segundo tipo, escape todos los caracteres de comilla doble ("""), si los hay, con dos caracteres de comilla doble consecutivos y escríbalo entre comillas dobles. 
  5. Inserte una cadena de yand ( `&` ) entre cada par de fragmentos adyacentes.
 
  Por ejemplo, si se usa el idioma de la interfaz de usuario de Office inglés (EE. UU.), si el formato de interfaz de usuario de una fórmula para un campo del tipo **ftConcat** es , donde es el nombre de un campo definido por el usuario, el formato estándar de dicha fórmula sería `text1 [Business Phone] "text2" [My custom field]` `My custom field` `""text1" & [_14856] & """text2""" & [My custom field]"` . 
  
## <a name="see-also"></a>Consulte también

- [FolderUserFields Stream Sample](folderuserfields-stream-sample.md)
- [Agregar una definición para un nuevo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)

