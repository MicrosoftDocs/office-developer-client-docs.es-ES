---
title: Estructuras de la secuencia de campos de carpeta
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
# <a name="folder-fields-stream-structures"></a>Estructuras de la secuencia de campos de carpeta

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La propiedad [PidTagUserFields](pidtaguserfields-canonical-property.md) de un mensaje contiene una secuencia binaria, FolderUserFields, que contiene las definiciones de los campos definidos por el usuario de la carpeta. En este tema se describen las estructuras de secuencia para las definiciones de campos definidos por el usuario de carpeta. 

Una estructura de secuencia FolderUserFields consiste en una estructura FolderUserFieldsA o FolderUserFieldsA seguida de una estructura FolderUserFieldsW.
  
Los elementos de datos de esta secuencia se almacenan inmediatamente a continuación de otros en el siguiente orden especificado:
  
- **FolderUserFieldsAnsi**: una estructura de secuencia FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (opcional): una estructura de secuencia FolderUserFieldsW.
    
La presencia de FolderUserFieldsUnicode se detecta por la longitud total del FolderUserFields mayor que la longitud de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi se usa para la compatibilidad con versiones anteriores, no Unicode, de clientes MAPI, por lo que, si FolderUserFieldsUnicode está presente, se omite el contenido de FolderUserFieldsAnsi. Para evitar una posible pérdida de datos en la conversión ANSI, al crear una secuencia FolderUserFields siempre incluya la parte FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Estructura de la secuencia FolderUserFieldsA

Una estructura de secuencia FolderUserFieldsA es una matriz de estructuras de secuencia FolderFieldDefinitionA que contiene definiciones para todos los campos definidos por el usuario en una carpeta de Outlook, a menos que se reemplace por la parte FolderUserFieldsW de la estructura FolderUserFields.
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el siguiente orden especificado:
  
- **FieldDefinitionCount**: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Este es el número de elementos de la matriz **FieldDefinitions** .
    
- **FieldDefinitions**: una matriz de estructuras de secuencia FolderFieldDefinitionA. El recuento de esta matriz es igual al elemento de datos **FieldDefinitionCount** .
    
A menos que la parte FolderUserFieldsW de la estructura FolderUserFields Reemplace esta FolderUserFieldsA, la matriz **FieldDefinitions** debe estar "terminada en NULL" al hacer que el último campo común. FieldType del elemento FolderFieldDefinitionA sea igual a a ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Estructura de la secuencia FolderUserFieldsW

Una estructura de secuencia FolderUserFieldsW es una matriz de estructuras de secuencia FolderFieldDefinitionW que contienen definiciones para todos los campos definidos por el usuario en una carpeta de Outlook.
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el siguiente orden especificado:
  
- **FieldDefinitionCount**: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Este es el número de elementos de la matriz **FieldDefinitions** .
    
- **FieldDefinitions**: una matriz de estructuras de secuencia FolderFieldDefinitionW. El recuento de esta matriz es igual al elemento de datos **FieldDefinitionCount** .
    
La matriz **FieldDefinitions** debe estar "terminada en NULL" haciendo que el campo Common. FieldType del último elemento de FolderFieldDefinitionW sea igual a ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Estructura de la secuencia FolderFieldDefinitionA

Una estructura de secuencia FolderFieldDefinitionA contiene una definición de un campo definido por el usuario con el nombre de campo almacenado en ANSI.
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el siguiente orden especificado:
  
- **FieldType**: FldType (4 bytes), el tipo de este campo.
    
- **FieldNameLength**: Word (2 bytes), el número de elementos de la matriz **FieldName** .
    
- **FieldName**: una matriz de Char. Esta es la representación de la página de códigos ANSI CP_ACP del nombre del campo. El recuento de esta matriz es igual a **FieldNameLength**. El nombre del campo debe cumplir con las restricciones del parámetro name tal como se especifica en el método [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, es posible que Outlook pueda controlar algunos valores de **FieldName** que no cumplen estas restricciones, pero estos casos no se tratan en este tema. 
  
- **Common**: una estructura de secuencia FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Estructura de la secuencia FolderFieldDefinitionW

Una estructura de secuencia FolderFieldDefinitionW contiene una definición de un campo definido por el usuario con el nombre de campo almacenado en Unicode.
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el siguiente orden especificado:
  
- **FieldType**: FldType (4 bytes), el tipo de este campo.
    
- **FieldNameLength**: Word (2 bytes), el número de elementos de la matriz **FieldName** .
    
- **FieldName**: una matriz de WCHAR. Esta es la representación Unicode (UTF-16) del nombre del campo. El recuento de esta matriz es igual a **FieldNameLength**. El nombre del campo debe cumplir con las restricciones del parámetro name tal como se especifica en el método [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, es posible que Outlook pueda controlar algunos valores de **FieldName** que no cumplen estas restricciones, pero estos casos no se tratan en este tema. 
  
- **Common**: una estructura de secuencia FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>Enumeración FldType

En la tabla siguiente se enumeran los valores de enumeración **FldType** . 
  
|Nombre|Valor|Significado|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Este tipo de campo se usa para terminar en NULL una matriz de definiciones de campo.  <br/> |
|ftString  <br/> |0x1  <br/> |Texto  <br/> |
|ftInteger  <br/> |0X3  <br/> |Entero  <br/> |
|ftTime  <br/> |0X5  <br/> |Fecha y hora  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Sí/No  <br/> |
|ftDuration  <br/> |0X7  <br/> |Duracion  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Palabras clave  <br/> |
|ftFloat  <br/> |0xC  <br/> |Número o porcentaje  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Moneda  <br/> |
|ftCalc  <br/> |0X12  <br/> |Formula  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinación de tipo que muestra sólo el primer campo que no está vacío y que omite los siguientes.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinación de tipos que se unen a los campos y los fragmentos de texto entre sí.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Estructura de la secuencia FolderFieldDefinitionCommon

Una estructura de secuencia FolderFieldDefinitionCommon contiene los datos de una definición de campos definidos por el usuario que es común a un FolderFieldDefinitionA y a un FolderFieldDefinitionW.
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el siguiente orden especificado:
  
- **PropSetGuid**: GUID (16 bytes), el GUID del conjunto de propiedades del nombre de la propiedad MAPI correspondiente al campo de la carpeta. El valor de este campo debe ser igual a PS_PUBLIC_STRINGS, a menos que el tipo de campo sea **ftNone** en cuyo caso el valor de este campo debe ser igual a GUID_NULL. 
    
   > [!NOTE]
   > Por motivos de compatibilidad heredada, Outlook puede ser capaz de controlar algunos valores de **PropSetGuid** que no cumplen esta restricción, aunque estos casos no se tratan en este tema. 
  
- **fcapm**: DWORD (4 bytes), una combinación de cero o más indicadores cuyos valores y significados se enumeran en la siguiente tabla. Las marcas con el mismo valor tienen significados que dependen del tipo de campo, es decir, del valor FldType.
    
    |Nombre de marca|Valor|Significado|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |El campo se puede editar.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |El campo se puede ordenar.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |El campo es agrupable.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |El campo puede contener varias líneas de texto.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Este campo del tipo ftFloat es un campo de porcentaje.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Este campo del tipo ftTime es un campo de hora de fecha y hora.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Para este campo del tipo ftInteger, no se permite ninguna unidad en formato de presentación; por ejemplo, formatos como "equipo-640 K..." no están permitidas.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |El campo se puede editar en el elemento: esto es específicamente para los formularios personalizados.  <br/> |
   
- **dwString**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **dwBitmap**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **dwDisplay**: DWORD (4 bytes). Vea la primera nota siguiente.
    
- **iFmt**: int (4 bytes). Para los tipos de campo que tienen el cuadro combinado "formato:" en los cuadros de diálogo "nuevo campo", "editar campo" y "propiedades de campo", el índice de base cero del formato seleccionado en ese cuadro combinado. Para los tipos de campo sin ese cuadro combinado, debe ser 0. El valor del campo, junto con el tipo de campo, determinan de forma única los valores de los campos **dwString**, **dwBitmap**y **DwDisplay** , vea la primera nota siguiente.
    
- **wszFormulaLength**: Word (2 bytes), el número de elementos de la matriz **wszFormulaLength** .
    
- **wszFormulaLength**: una matriz de WCHAR. Esta es la representación Unicode (UTF-16) de la cadena de fórmulas del campo en su formato estándar. Vea la segunda nota siguiente para obtener la descripción de los formatos estándar y de interfaz de usuario de la fórmula de un campo. El recuento de esta matriz es igual a **wszFormulaLength**. La cadena de fórmula debe ser una cadena vacía a menos que el tipo de campo sea **ftCalc**, **ftSwitch** o **ftConcat**.
    
> [!NOTE]
> Aunque los valores de **dwString**, **dwBitmap**y **dwDisplay** se determinan de forma exclusiva en función del valor de **FldType** y el valor de **iFmt** , que son redundantes, los valores correctos siguen siendo necesarios para las correcciones correctas. procesamiento de la definición del campo por parte de Outlook. No hay ninguna descripción sencilla del algoritmo que realice esta determinación. 
> 
> Por lo tanto, para averiguar qué valores de **dwString**, **dwBitmap**y **dwDisplay** corresponden a un valor de **FldType** y un valor de **iFmt** dados, realice una prueba creando un campo definido por el usuario de ese tipo y con ese formato seleccionado. en el cuadro combinado **formato** , asumiendo su aplicabilidad, inspeccione la secuencia **FolderUserFields** resultante que Outlook crea para el campo definido por el usuario. 
  
La fórmula del campo en su formato de interfaz de usuario se modifica en el cuadro de texto **fórmula** de los cuadros de diálogo **nuevo campo**, **Editar campo**y **propiedades de campo** para el campo definido por el usuario. El algoritmo para convertir una fórmula del formato de la interfaz de usuario al formato estándar depende del tipo de campo, tal y como se describe en lo siguiente: 
- Para los campos de tipos **ftCalc** y **ftSwitch**, el formato estándar para campos integrados, las propiedades MAPI correspondientes no se denominan propiedades de la cadena Kind\_MNID, se obtienen reemplazando los fragmentos de nombre de campo `[<field_name>]` , que es con fragmentos `[_<field_dispid_decimal>]`. 

  Por ejemplo, si el formato de interfaz de usuario de una fórmula para un campo de la **fórmula**de tipo, que es **ftCalc**, el idioma de la interfaz de `[Business Phone] & [My custom field]`usuario de `My custom field` Office que va a ser inglés norteamericano es, donde es el nombre de un campo definido por el usuario, el formato estándar de dicha fórmula sería `[_14856] & [My custom field]`.

- Para los campos de tipo **ftConcat**, el formato estándar se obtiene al realizar lo siguiente:

  1. Truncar espacios en blanco iniciales y finales. 
  2. Analice la fórmula en una secuencia de fragmentos de los dos tipos siguientes: 
     - Un nombre de campo entre corchetes, es decir `[<field_name>]`,. 
     - Una subcadena que no contiene corchetes.   
      Asegúrese de que no hay dos fragmentos del segundo tipo adyacentes en la secuencia. Si la fórmula no se puede analizar de esta manera, se considera no válida. 
  3. Realice el mismo reemplazo para los fragmentos del primer tipo de los campos **ftCalc** y **ftSwitch** . 
  4. Para cada fragmento del segundo tipo, tiene que escapar todos los caracteres de comillas dobles ("" "), si los hay, con dos caracteres de comillas dobles consecutivos y encerrarla entre comillas dobles. 
  5. Inserta una cadena de y`&`comercial () entre cada par de fragmentos adyacentes.
 
  Por ejemplo, con el idioma de la interfaz de usuario de Office inglés (Estados Unidos), si el formato de la interfaz de `text1 [Business Phone] "text2" [My custom field]`usuario de `My custom field` una fórmula para un campo del tipo **ftConcat** es, donde es el nombre de un campo definido por `""text1" & [_14856] & """text2""" & [My custom field]"`el usuario, el formato estándar de dicha fórmula sería. 
  
## <a name="see-also"></a>Vea también

- [Ejemplo de secuencia FolderUserFields](folderuserfields-stream-sample.md)
- [Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)

