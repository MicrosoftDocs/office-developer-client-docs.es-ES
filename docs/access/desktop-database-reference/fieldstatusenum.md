---
title: FieldStatusEnum (referencia de base de datos de escritorio de Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ccf98f2a740e2a077d6e2451102bfc72bcd1b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292520"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum

**Se aplica a:** Access 2013, Office 2013

Especifica el estado de un objeto **Field**.

Los valores **adFieldPending\*** indican la operación que provocó el estado, y se pueden combinar con otros valores de estado.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldAlreadyExists</strong></p></td>
<td><p>26</p></td>
<td><p>Indica que ya existe el campo especificado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12 </p></td>
<td><p>Indica que se envió al proveedor OLE DB un valor de estado no válido desde ADO. Entre otras causas posibles, se incluyen un proveedor OLE DB 1.0 o 1.1 o una combinación incorrecta de <a href="value-property-ado.md">Value</a> y de <a href="status-property-ado-field.md">Status</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p>Indica que el servidor de la dirección URL especificada por <a href="source-property-ado-record.md">Source</a> no pudo completar la operación.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>Indica una operación en la que un árbol o un subárbol se movió a una ubicación nueva pero no se pudo eliminar el origen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2 </p></td>
<td><p>Indica que el campo no se puede recuperar ni almacenar sin pérdida de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCantCreate</strong></p></td>
<td><p>7 </p></td>
<td><p>Indica que no se pudo agregar el campo a causa de que el proveedor superó una limitación (como el número de campos admitidos).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6 </p></td>
<td><p>Indica que los datos devueltos por el proveedor desbordaron el tipo de datos del campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13 </p></td>
<td><p>Indica que se utilizó el valor predeterminado del campo al establecer los datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16 </p></td>
<td><p>Indica que no existe el campo especificado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15 </p></td>
<td><p>Indica que se omitió este campo al establecer los valores de los datos en el origen. El proveedor no estableció ningún valor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10  </p></td>
<td><p>Indica que no se puede modificar el campo porque es una entidad calculada o derivada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17 </p></td>
<td><p>Indica que la dirección URL del origen de datos contiene caracteres no válidos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3 </p></td>
<td><p>Indica que el proveedor devolvió un valor VARIANT de tipo VT_NULL y que el campo no está vacío.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Valor predeterminado. Indica que el campo se agregó o se eliminó correctamente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Indica que el proveedor no puede obtener suficiente espacio de almacenamiento para completar una operación de copia o movimiento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingChange</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indica que el valor del campo ha sido eliminado y luego agregado de nuevo, quizá con un tipo de datos diferente, o que el valor del campo que antes tenía un estado adFieldOK ha cambiado. La forma final del campo modificará la colección <a href="fields-collection-ado.md">Fields</a> después de llamar al método <a href="update-method-ado.md">Update</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Indica que la operación <strong>Delete</strong> provocó el establecimiento del estado. El campo ha sido marcado para su eliminación de la colección <strong>Fields</strong> después de la llamada al método <strong>Update</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indica que la operación <strong>Append</strong> provocó el establecimiento del estado. El objeto <strong>Field</strong> (campo) ha sido marcado para su eliminación de la colección <strong>Fields</strong> después de la llamada al método <strong>Update</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Indica que el proveedor no puede determinar qué operación causó el establecimiento del estado del campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Indica que el proveedor no puede determinar qué operación causó el establecimiento del estado del campo, y que el campo se eliminará de la colección <strong>Fields</strong> después de la llamada al método <strong>Update</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9 </p></td>
<td><p>Indica que no se puede modificar el campo debido a que se ha definido como de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>Indica que el campo del origen de datos se ha definido como de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>Indica que el proveedor no pudo realizar la operación porque ya existe un objeto en la dirección URL de destino y no es posible sobrescribir el objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18 </p></td>
<td><p>Indica que el proveedor no pudo realizar la operación a causa de que el origen de datos está bloqueado por otros procesos o aplicaciones.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>Indica que una dirección URL de origen o destino está fuera del ámbito del registro actual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Indica que el valor no cumplió la restricción del esquema del origen de datos para el campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5 </p></td>
<td><p>Indica que el valor de datos devuelto por el proveedor tenía signo, pero el tipo de datos del valor del campo ADO no.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4 </p></td>
<td><p>Indica que se truncaron datos de longitud variable al leer el origen de datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8 </p></td>
<td><p>Indica que el proveedor no pudo determinar el valor al leer el origen de datos. Por ejemplo, la fila estaba recién creada, el valor predeterminado de la columna no estaba disponible y no se había aún especificado un nuevo valor.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p> 21</p></td>
<td><p>Indica que el proveedor no puede encontrar el volumen de almacenamiento indicado por la dirección URL.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente de ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

