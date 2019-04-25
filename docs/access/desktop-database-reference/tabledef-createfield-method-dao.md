---
title: Método TableDef.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308445"
---
# <a name="tabledefcreatefield-method-dao"></a>Método TableDef.CreateField (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[Field](field-object-dao.md)** (solo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)

*expression* Variable que representa un objeto **TableDef**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una cadena que asigna nombres únicos al nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más detalles sobre los nombres de <strong>Field</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante que determina el tipo de datos del nuevo objeto<strong>Field</strong>. Consulte la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener los tipos de datos válidos.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Un Entero que indica el tamaño máximo, en bytes, de un objeto <strong>Field</strong> que contiene texto. Consulte la propiedad <strong><a href="field-size-property-dao.md">Size</a></strong> para obtener valores de tamaño válidos. Se omite este argumento para los campos numéricos y de ancho fijo.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Field

## <a name="remarks"></a>Observaciones

Puede usar el método **CreateField** para crear un nuevo campo, así como para especificar el nombre, el tipo de datos y el tamaño del campo. Si omite una o más partes opcionales al usar **CreateField**, puede usar una instrucción de asignación adecuada para configurar o restablecer la propiedad correspondiente antes de anexar el nuevo objeto a la colección. Tras anexar el nuevo objeto, puede modificar algunas, pero no todas, las configuraciones de la propiedad. Consulte los temas de propiedades individuales para obtener más detalles.

Los argumentos type y size se aplican sólo a objetos **Field** de un objeto **TableDef**. Estos argumentos se omiten cuando se asocia un campo **Field** con un objeto **Index** o **Relation**.

Si Name hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)**.

Para eliminar un objeto **Field** de una colección **Fields**, use el método **[Delete](fields-delete-method-dao.md)** de una colección. No puede eliminar un objeto **Field** de una colección **Fields** de un objeto **TableDef** después de crear un índice que hace referencia al campo.

**Vínculo proporcionado por** la comunidad de [UtterAccess](https://www.utteraccess.com). UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.

- [Agregar un campo de hipervínculo a una tabla existente con DAO](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

