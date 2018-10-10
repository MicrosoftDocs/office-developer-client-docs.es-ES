---
title: Inicializar el controlador de orígenes de datos de Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f711e9814e32742c89c37ae3357111143ca18b6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483422"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Inicializar el controlador de orígenes de datos de Microsoft Exchange

**Se aplica a**: Access 2013 | Office 2013

Cuando se instala el controlador de orígenes de datos de Microsoft® Exchange, el programa de instalación escribe un conjunto de valores predeterminados en el Registro de Microsoft Windows®, concretamente en las subclaves Engines e ISAM Formats. No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación. Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de orígenes de datos de Microsoft® Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Configuración de inicialización del origen de datos de Microsoft Exchange

La **Access Connectivity Engine\\motores\\Exchange** carpeta incluye la configuración de inicialización para el controlador Aceexch.dll, utilizado para el acceso externo a las carpetas de Microsoft Outlook y Microsoft Exchange. La única entrada de esta carpeta es la siguiente:

`win32=<path>\ACEEXCH.DLL`

El motor de base de datos de Microsoft Access utiliza este valor para indicar la ubicación de Aceexch.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG\_SZ.

Los resultados de utilizar el formato ISAM de Outlook y el formato ISAM del cliente de Exchange son similares. La única diferencia estriba en que los dos clientes utilizan nombres distintos para las mismas columnas. Ambos formatos ISAM se han creado con objeto de que el motor de base de datos de Microsoft Access pueda devolver los nombres de las columnas en el estilo determinado por el usuario.

## <a name="microsoft-outlook-client-isam-formats"></a>Formatos ISAM del cliente de Microsoft Outlook

La **Access Connectivity Engine\\formatos ISAM de\\Outlook 9.0** carpeta contiene las siguientes entradas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.



## <a name="microsoft-exchange-client-isam-formats"></a>Formatos ISAM del cliente de Microsoft Exchange

La **Access Connectivity Engine\\formatos ISAM de\\Exchange 4.0** carpeta contiene las siguientes entradas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Personalizar el archivo Schema.ini para los datos de Outlook y de Exchange

Outlook y Exchange utilizan el archivo Schema.ini casi de la misma manera que el ISAM de texto. Dicho archivo contiene los detalles de un origen de datos: cómo se da formato a los datos y los nombres de las columnas a las que se debe tener acceso.

No es necesario modificarlo para poder leer, importar o exportar datos para Outlook y Exchange. Muchos de los valores incluidos en él para Outlook y Exchange son específicos de etiquetas internas requeridas por MAPI. No debe intentar modificar dichos valores de etiqueta.

