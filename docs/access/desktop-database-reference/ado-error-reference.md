---
title: Referencia de errores en ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283397"
---
# <a name="ado-error-reference"></a>Referencia de errores en ADO

**Se aplica a:** Access 2013, Office 2013

La constante **ErrorValueEnum** describe los valores de error en ADO. Para consultar una lista completa de estas constantes enumeradas, incluyendo sus valores, vea [Apéndice B: Errores de ADO](appendix-b-ado-errors.md). En esta sección, se examinan algunos de los errores más interesantes y se explican algunas situaciones específicas que pueden causarlos, o soluciones para corregir el problema. Se indica la constante **ErrorValueEnum** y el número decimal positivo corto.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Número</p></th>
<th><p>Constante ErrorValueEnum</p></th>
<th><p>Descripción/Causas posibles</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>El proveedor no pudo realizar la operación solicitada.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Los argumentos son del tipo incorrecto, están fuera del intervalo aceptable o están en conflicto entre sí. Este error se produce a menudo por un error tipográfico en una instrucción SQL SELECT. Por ejemplo, un nombre de campo o de tabla mal escrito puede generar este error. Este error también se puede producir cuando no existe en el almacén de datos un campo o una tabla que se menciona en una instrucción SELECT.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>No se pudo abrir un archivo. Se especificó un nombre de archivo mal escrito, o se movió, cambió o eliminó un archivo. En una red, podría ser que la unidad no estuviese disponible temporalmente o que el tráfico en la red impidiese una conexión.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>No se pudo leer un archivo. El nombre del archivo se ha especificado incorrectamente, el archivo se puede haber movido o eliminado, o el archivo se puede haber dañado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Error de escritura en un archivo. Tal vez haya cerrado un archivo y después intentado escribir en él, o el archivo podría estar dañado. Si el archivo está en una unidad de red, ciertas condiciones transitorias de la red podrían impedir la escritura en una unidad de red.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p><strong>BOF</strong> o <strong>EOF</strong> es True, o bien el registro actual se ha eliminado. La operación solicitada requiere un registro actual. Se realizó un intento de actualizar registros mediante <strong>Find</strong> o <strong>Seek</strong> para mover el puntero de registros al registro deseado. Si no se encuentra el registro, <strong>EOF</strong> será True. Este error también se puede producir después de un error de <strong>AddNew</strong> o <strong>Delete</strong> porque, cuando estos métodos generan errores, no hay registro activo.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>Operación no permitida en este contexto.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>El proveedor suministrado es distinto del que se está utilizando.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>No se puede cerrar explícitamente un objeto <strong>Connection</strong> durante una transacción. No se puede cerrar un objeto <strong>Recordset</strong> o <strong>Connection</strong> que esté participando en una transacción. Llame a <strong>RollbackTrans</strong> o a <strong>CommitTrans</strong> antes de cerrar el objeto.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>El objeto o el proveedor no es capaz de realizar la operación solicitada. Algunas operaciones dependen de una versión de proveedor determinada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>No se puede encontrar un elemento en la colección correspondiente al nombre o el ordinal solicitado. Se ha especificado un nombre de campo o de tabla incorrecto.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>El objeto ya está en la colección. No se puede anexar. Un objeto no se puede agregar dos veces a la misma colección.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>El objeto ya no es válido.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>La aplicación utiliza un valor de tipo incorrecto para la operación actual. Tal vez haya proporcionado una cadena a una operación que espera, por ejemplo, una secuencia.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>La operación no está permitida si el objeto está cerrado. Se cerró <strong>Connection</strong> o <strong>Recordset</strong>. Por ejemplo, puede ser que alguna otra rutina haya cerrado un objeto global. Este error se puede evitar comprobando la propiedad <strong>State</strong> antes de intentar realizar una operación.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>La operación no está permitida si el objeto está abierto. No se puede abrir un objeto que ya está abierto. No se pueden anexar campos a un <strong>conjunto de registros</strong> abierto.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>No se encuentra el proveedor. Puede que no esté instalado correctamente. Tal vez no se haya especificado correctamente el nombre del proveedor, o no se haya instalado el proveedor especificado en el equipo donde se está ejecutando el código, o se haya dañado la instalación.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>No se puede cambiar la propiedad <strong>ActiveConnection</strong> de un objeto <strong>Recordset</strong> que tiene un objeto <strong>Command</strong> como origen. La aplicación intentó asignar un objeto <strong>Connection</strong> nuevo a un <strong>conjunto de registros</strong> que tiene un objeto <strong>Command</strong> como origen.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>El objeto <strong>Parameter</strong> no se ha definido correctamente. Se proporcionó información incoherente o incompleta.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>No se puede utilizar la conexión para realizar esta operación. Está cerrada o no es válida en este contexto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>No se puede realizar la operación mientras se procesa el evento. No se puede realizar una operación dentro de un controlador de eventos que provoca que se desencadene el evento de nuevo. Por ejemplo, no se debe llamar a métodos de navegación desde dentro de un controlador de eventos <strong>WillMove</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>No se puede realizar la operación mientras se ejecuta asincrónicamente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>La operación ha sido cancelada por el usuario. La aplicación ha llamado al método <strong>CancelUpdate</strong> o <strong>CancelBatch</strong> y se ha cancelado la operación en curso.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>No se puede realizar la operación mientras se conecta asincrónicamente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>La transacción de coordinación no es válida o no se ha iniciado.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>No se puede realizar la operación mientras no se ejecute.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>La configuración de seguridad de este equipo prohíbe el acceso a un origen de datos en otro dominio.</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>Para uso interno exclusivamente. No utilizar (la entrada se ha incluido para ofrecer una información completa; este error no debería aparecer en su código).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>Para uso interno exclusivamente. No utilizar (entrada incluida para ofrecer una información completa; este error no debería aparecer en su código).</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>El valor de los datos entra en conflicto con las restricciones de integridad del campo. Un valor nuevo para un <strong>campo</strong> generaría una clave duplicada. Un valor que conforma un lado de una relación entre dos registros podría no ser actualizable.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>No se tienen suficientes permisos para escribir en el campo. El usuario mencionado en la cadena de conexión no tiene los permisos apropiados para escribir en un <strong>campo</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>El valor de los datos es demasiado grande para poder representarlo mediante el tipo de datos del campo. Se asignó un valor numérico que es demasiado grande para el campo correspondiente. Por ejemplo, un valor entero largo se asignó a un campo numérico entero corto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>El valor de los datos está en conflicto con el tipo de datos o las restricciones del campo. El almacén de datos tiene restricciones de validación que difieren del valor del <strong>campo</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>La conversión produjo un error porque el valor de los datos tenía signo y el tipo de datos del campo utilizado por el proveedor no tenía signo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>El valor de los datos no se puede convertir por motivos distintos a un desajuste entre signos o a un desbordamiento de datos. Por ejemplo, puede que la conversión haya truncado datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>No se puede establecer ni recuperar el valor de los datos porque el tipo de datos del campo era desconocido o el proveedor no tenía suficientes recursos para realizar la operación.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>El registro no contiene este campo. Se especificó un nombre de campo incorrecto o se hizo referencia a un campo no incluido en la colección <strong>Fields</strong> del registro activo.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>No existe la dirección URL de origen o la dirección URL del elemento principal de destino. Hay un error tipográfico en la dirección URL de origen o de destino. Es posible que https://mysite/photo/myphoto.jpg tenga cuándo debería tenerla en su https://mysite/photos/myphoto.jpg lugar. El error tipográfico en la dirección URL primaria (en este caso, <em>photo</em> en lugar de <em>photos</em>) causó un error.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>No se tienen suficientes permisos para obtener acceso a un árbol o a un subárbol. El usuario mencionado en la cadena de conexión no tiene los permisos adecuados.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>La dirección URL contiene caracteres no válidos. Asegúrese de que la dirección URL está escrita correctamente. La dirección URL sigue el esquema registrado para el proveedor actual (por ejemplo, Internet Publishing Provider está registrado para http).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>El objeto representado por la dirección URL especificada está bloqueado por uno o varios procesos diferentes. Espere hasta que el proceso haya finalizado e intente de nuevo la operación. El objeto al que trata de tener acceso ha sido bloqueado por otro usuario o por otro proceso de su aplicación. Esto suele ocurrir en un entorno multiusuario.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>No se puede realizar una operación de copia. El objeto mencionado en la dirección URL de destino ya existe. Especifique <strong>adCopyOverwrite</strong> para reemplazar el objeto. Si no especifica <strong>adCopyOverwrite</strong> cuando copie los archivos a un directorio, se producirá un error al intentar copiar un elemento que ya exista en la ubicación de destino.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>El servidor no puede completar la operación. Puede deberse a que el servidor esté ocupado con otras operaciones, o a que tenga un bajo nivel de recursos.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>El proveedor no puede encontrar el dispositivo de almacenamiento que indica la dirección URL. Compruebe que la dirección URL está escrita correctamente. La dirección URL del dispositivo de almacenamiento podría no ser correcta, pero este error puede deberse a otros motivos. El dispositivo podría estar desconectado, o un elevado volumen de tráfico en la red podría impedir el establecimiento de la conexión.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>No se puede realizar operación. El proveedor no puede obtener suficiente espacio de almacenamiento. Podría no haber suficiente memoria RAM o espacio en disco para archivos temporales del servidor.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>La dirección URL de origen o de destino está fuera del alcance del registro activo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>La operación no se pudo completar y el estado no está disponible. Tal vez el campo no esté disponible o no se haya intentado la operación. Otro usuario podría haber cambiado o eliminado el campo al que está intentando obtener acceso.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>No existe el registro mencionado en esta dirección URL. Al intentar abrir un archivo utilizando un objeto <strong>Record</strong>, no se escribió correctamente el nombre de archivo o la ruta de acceso al archivo.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>La dirección URL del objeto que se va a eliminar está fuera del alcance del registro activo.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>La operación requiere un <strong>ParentCatalog</strong> válido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>Se denegó la conexión. La conexión nueva que solicitó tiene características diferentes que la que se está utilizando.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>Error en la actualización de campos. Para obtener más información, examine la propiedad <strong>Status</strong> de objetos de campo individuales. Este error puede producirse en dos situaciones: al cambiar el valor de un objeto <strong>Field</strong> durante el proceso de cambio o inclusión de un registro en la base de datos, y al cambiar las propiedades del propio objeto <strong>Field</strong>. Hubo un error en la actualización de <strong>Record</strong> o <strong>Recordset</strong> debido a un problema con uno de los campos en el registro actual. Enumere la colección <strong>Fields</strong> y compruebe la propiedad <strong>Status</strong> de cada campo para determinar la causa del problema.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>El proveedor no admite restricciones compartidas. Se ha realizado un intento de restringir un uso compartido de archivos y su proveedor no admite el concepto.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>El proveedor no admite el tipo restricciones compartidas solicitado. Se realizó un intento de establecer un tipo determinado de restricción de uso compartido de archivos que no admite su proveedor. Vea la documentación del proveedor para determinar qué restricciones de uso compartido de archivos se admiten.</p></td>
</tr>
</tbody>
</table>

