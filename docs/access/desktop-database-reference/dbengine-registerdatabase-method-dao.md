---
title: DBEngine.RegisterDatabase (método) (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715609"
---
# <a name="dbengineregisterdatabase-method-dao"></a>DBEngine.RegisterDatabase (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Proporciona información de conexión para un origen de datos ODBC en el Registro de Windows. El controlador ODBC necesita información de conexión cuando se abre el origen de datos ODBC durante una sesión.

## <a name="syntax"></a>Sintaxis

*expresión* . RegisterDatabase (***Dsn***, ***controlador***, ***silenciosa***, ***atributos***)

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="parameters"></a>Parámetros

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
<td><p><em>DSN</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>Nombre utilizado en el método <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>. Se refiere a un bloque de información descriptiva sobre el origen de datos. Por ejemplo, si el origen de datos es una base de datos remota ODBC, podría ser el nombre del servidor.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>Nombre del controlador ODBC. Éste no es el nombre del archivo DLL del controlador ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><em>Silenciosa</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p><strong>True</strong> si no desea mostrar los cuadros de diálogo del controlador ODBC que solicitan información específica del controlador; o <strong>False</strong> si desea mostrar los cuadros de diálogo del controlador ODBC. Si silent es <strong>True</strong>, attributes debe contener toda la información necesaria específica del controlador o se muestran los cuadros de diálogo de todos modos.</p></td>
</tr>
<tr class="even">
<td><p><em>Atributos</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>Lista de palabras clave que se deben agregar al Registro de Windows. Las palabras clave están en una cadena delimitada por retornos de carro.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Si la base de datos ya está registrada (ya se ha proporcionado la información de conexión) en el Registro de Windows cuando utiliza el método **RegisterDatabase**, la información de conexión está actualizada.

Si el método **RegisterDatabase** provoca un error por algún motivo, no se han realizado cambios en el Registro de Windows y se produce un error.

Para obtener más información sobre los controladores ODBC como SQL Server, vea el archivo de Ayuda suministrado con el controlador.

## <a name="example"></a>Ejemplo

En este ejemplo se utiliza el método **RegisterDatabase** para registrar un origen de datos Microsoft SQL llamado Publishers en el Registro de Windows.

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

