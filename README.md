# testes
testes do desafio dio
// Arquivo ValidacoesListaTests.cs

using System;
using System.Collections.Generic;
using Xunit;

namespace TestesUnitarios.Desafio.Tests
{
    public class ValidacoesListaTests
    {
        [Fact]
        public void RemoverNumerosNegativos_DeveRemoverNumerosNegativos()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var numeros = new List<int> { -3, 5, -8, 10, -2 };

            // Act
            var resultado = validacoesLista.RemoverNumerosNegativos(numeros);

            // Assert
            Assert.Equal(new List<int> { 5, 10 }, resultado);
        }

        [Fact]
        public void ListaContemDeterminadoNumero_DeveRetornarTrueSeNumeroPresente()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var numeros = new List<int> { 1, 3, 5, 7, 9 };

            // Act
            var resultado = validacoesLista.ListaContemDeterminadoNumero(numeros, 5);

            // Assert
            Assert.True(resultado);
        }

        [Fact]
        public void ListaContemDeterminadoNumero_DeveRetornarFalseSeNumeroNaoPresente()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var numeros = new List<int> { 1, 3, 5, 7, 9 };

            // Act
            var resultado = validacoesLista.ListaContemDeterminadoNumero(numeros, 4);

            // Assert
            Assert.False(resultado);
        }

    }
}
